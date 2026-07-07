# Sample Receipt

A SWECore-style receipt should make the reviewer’s job easier. It should
separate what changed, what evidence exists, what is still limited, and what
should happen next.

```text
Task: Add waitlist email validation.

Scope: Form validation and tests only.

Changed: Validation rule and related test.

Evidence: Tests passed / or bounded warning.

Claim boundary: Not production-ready unless production evidence exists.

Reviewer next step: Inspect validation logic and run the listed test command.

Not proven: Deliverability, abuse resistance, or full production readiness.
```

## Why this matters

AI-assisted work can look finished before the evidence is clear. A receipt helps
slow down the trust decision and shows the reviewer what is actually known.

## What reviewers get

Reviewers get a compact summary of scope, changed surface, evidence, claim
limits, and the next inspection step.

## What this does not prove

A sample receipt does not prove production readiness, abuse resistance,
deliverability, security certification, or compliance certification. It is a
review aid, not a replacement for stronger validation.
