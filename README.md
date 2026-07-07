# SWECore

SWECore is a local-first governance and evidence layer for AI-assisted software
delivery.

SWECore helps teams and serious individual builders review AI-assisted code
changes with visible scope, evidence, receipts, and known limits before the
change is trusted.

## What SWECore helps with

- Scope before trust: make the intended change visible before reviewing it.
- Evidence before claims: separate proof, warnings, and unsupported claims.
- Reviewer-ready handoff: show what changed, what to inspect, and what remains
  unproven.
- Local-first / BYOK-oriented workflow: keep governance close to the repository
  and let teams choose their own AI tooling and provider posture.
- Early-access data boundary: keep intake low-sensitivity and avoid private
  repository or secret collection.

## What SWECore is not

- Not a coding agent.
- Not an IDE.
- Not a model wrapper.
- Not a prompt marketplace.
- Not a hosted dashboard today.
- Not production-ready or compliance-ready today.

## Who it is for

- Solo Pro: solo technical founders and serious individual builders carrying
  product, code, review, and delivery responsibility alone.
- Team: small teams adopting coding agents.
- Business: groups validating AI-code governance before broader rollout.
- Enterprise / Regulated: roadmap-only conversation until stronger proof exists.

## The review loop

1. Scope the change.
2. Attach evidence.
3. Block unsupported claims.
4. Produce a reviewer-ready receipt.
5. Decide next action.

## Example receipt

```text
Task: Add waitlist email validation.

Scope: Form validation and tests only.

Changed: Validation rule and related test.

Evidence: Tests passed / or bounded warning.

Claim boundary: Not production-ready unless production evidence exists.

Reviewer next step: Inspect validation logic and run the listed test command.

Not proven: Deliverability, abuse resistance, or full production readiness.
```

## Early access

- [Product](https://swecore.dev)
- [Demo](https://swecore.dev/demo)
- [Pricing](https://swecore.dev/pricing)
- [Trust](https://swecore.dev/trust)
- [Docs](https://swecore.dev/docs)
- [Early access](https://swecore.dev/early-access)

## Current status

Early access. No checkout. Pricing and packaging may change.

## Claim boundaries

This repository does not claim:

- production-ready, MVP-ready, or launch-ready status;
- security-ready or compliance-ready status;
- SOC 2 ready, ISO 27001 ready, GDPR-ready, KVKK-ready, or AI Act-ready status;
- enterprise-ready status;
- immutable audit;
- hosted dashboard availability;
- enterprise control plane availability;
- automatic delivery validation;
- automatic CLI or mobile remediation;
- full runner parity;
- full SWECore runtime public shipment.

## Repository boundary

This public repository is a product showcase and documentation surface, not the
full commercial runtime. It should explain the product boundary without exposing
internal runtime details, commercial pack internals, private planning material,
or sensitive implementation details.

## License

No license file is currently present in this repository. Unless a license is
added, default copyright restrictions apply.
