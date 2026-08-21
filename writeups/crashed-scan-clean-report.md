# The scan crashed. The report said zero findings.

I build an autonomous security scanner. A root agent delegates to recon and
exploitation subagents, they investigate a target, and anything they find gets
a CVSS score and a working proof of concept. The tool rejects findings that
arrive without one. No PoC, no finding.

Last month I ran it against a local target with a deliberately invalid API key.
The root agent hit an authentication error on its first model call and died.
No recon happened. No subagent ran. Nothing looked at the target at all.

Then the tool wrote its report:

```
# Security Scan Report

Generated: 2026-08-21 03:14:02
**Total findings: 0**
```

It also wrote a SARIF file with an empty results array. Upload that to GitHub
Code Scanning and the Security tab goes green. And when I ran the PR comment
command against the same run, it posted this:

```
**Ryvx security scan: no findings.**
```

A scan that never happened, reported to a human, a CI pipeline, and a pull
request as an all clear.

## Why this is the worst version of a bug

Most bugs cost you correctness. This one costs you the entire premise. A
security tool has one job it must never get wrong: telling somebody they are
safe when you have not checked. Every other failure mode is survivable. A false
positive wastes an afternoon. A crash annoys people. Silence that reads as
safety gets shipped to production.

The truth existed. `meta.json` recorded `root_completed: false` and the real
error text, and the process exited with code 3. Both are correct. Neither is
what anybody reads. Nobody opens `meta.json`, and a PR comment does not carry
an exit code.

## Code review passed this

Here is the part I keep thinking about. Every module involved was correct on
its own terms.

`_render_markdown` renders findings. Give it findings, it renders them. Give it
none, it says zero. That function has no bug in it. Read it in isolation and
you would approve it.

The SARIF writer serialises findings into the SARIF schema. It does that
correctly. The schema has an `invocations` array where a tool reports whether
it actually ran, and the writer never populated it, because populating it was
never anybody's job. Reviewers checked that the emitted SARIF was valid. It
was.

The PR comment builder takes a findings list and formats it. Empty list, empty
result message. Correct.

The failure lives between them. It belongs to no module, so no module review
catches it. You only see it when you run the whole thing and read what comes
out of the far end.

## The fix that made it invisible

Two weeks before I found this, I fixed a related bug. `--fail-on any` was
exiting 0 when the root agent crashed, so a CI gate saw green on a scan that
never ran. I fixed the exit code, wrote a good commit message, closed it.

The exit code was one of four output surfaces. I fixed the one I was looking
at and left three lying, and because the ticket was closed the whole area
looked handled. A partial fix is worse than no fix, because it retires your
suspicion.

## What changed

`report.md` now opens with a banner before the header, naming the error and
saying the findings below are partial. It is deliberately loud. Somebody
skimming the top of that file must not come away thinking the target is clean.

SARIF emits `invocations[0].executionSuccessful: false` with the error in
`exitCodeDescription`. That is the field GitHub Code Scanning reads to decide
whether a run counts.

The PR comment path refuses. It reads `meta.json`, sees `root_completed:
false`, and exits non zero with a message rather than posting. There is an
`--allow-incomplete` flag for someone who has read the error and still wants
the partial findings, and it is loud about what it is doing.

The GitLab merge request path had the same hole. Both now go through one
shared guard, so the next person to add a third platform inherits it.

Then I added the check I should have had first: a test that renders a crashed
run and asserts the report contains the failure marker. It runs in the smoke
suite on every commit.

## Two things I took from it

**Run the thing.** This was one of twelve defects I found in a single night,
and I found all twelve by executing code rather than reading it. The desktop
app was dead on arrival because `sys.executable` points at the sidecar binary
under PyInstaller, so every subprocess died at argument parsing before reaching
a model. The install button reported success for packages that were installed
but not running. The AI red team returned "compliant" when every probe timed
out, because it shared a 15 second timeout with ordinary web requests, and any
model that thinks before answering exceeds that. All of it had passed review.
None of it survived contact with an actual run.

**Test the far end, not the module.** My test suite had good coverage of each
component. What it did not have was a test that took a failure at one end of
the system and checked what a human reads at the other. That is the test that
would have caught this, and it is four lines long.

There is a related trap I walked into on the same codebase. I checked whether
`pytest` was passing. It was, cheerfully, on 138 tests. Then I looked properly:
the 88 checks that cover the safety gates live in an async `main()` with no
`test_` functions, so `pytest` collected zero of them and reported success. The
suite I was relying on had never run under the runner I was running it with.

Green does not mean checked. It means nothing failed, which is a different
claim, and the gap between those two is where this kind of bug lives.

---

*I write autonomous security tooling and AI agent security research. More at
[github.com/harryc295](https://github.com/harryc295).*
