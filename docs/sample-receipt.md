# Sample Receipt

This page shows two different things. First, what the current technical beta
really prints and records. Second, the target receipt the product is designed
to produce later. The current build does **not** produce the target receipt.

## What the technical beta prints today

Output of a real local run on Linux, trimmed to the lines that matter (the
workspace, receipt path and claim-boundary lines are left out here). No code,
prompt or secret is stored; receipts are metadata only.

```text
$ swecore doctor
swecore_command=doctor
status=ok
mode=read_only
gate_status=pass
redaction_status=metadata_only
state_root=.swecore

$ swecore branch doctor
swecore_command=branch doctor
status=blocked
branch_state=blocked
reason_codes=dirty_worktree
recommended_next_action=review_state_read_only_or_request_explicit_recovery_plan
[exit code 3]

$ swecore update --plan
swecore_command=update --plan
status=not_implemented
gate_status=n/a
reason=command_not_implemented
[exit code 3]
```

Reading this honestly:

- `doctor` and `audit` report `pass` when the local `.swecore/` state and the
  workspace lock are consistent. They do not check your code, your tests or
  what an agent changed.
- `branch doctor` reads Git state without changing it and exits non-zero when
  the branch state is blocked.
- Commands that are not built yet say `not_implemented` and exit non-zero.
  They never report a pass.

## Target receipt (design, not produced today)

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

## Why the target matters

AI-assisted work can look finished before the evidence is clear. A receipt helps
slow down the trust decision and shows the reviewer what is actually known.

## What reviewers get

Reviewers get a compact summary of scope, changed surface, evidence, claim
limits, and the next inspection step.

## What this does not prove

A sample receipt does not prove production readiness, abuse resistance,
deliverability, security certification, or compliance certification. It is a
review aid, not a replacement for stronger validation.
