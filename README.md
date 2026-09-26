# SWECore

SWECore is a local-first governance and evidence layer for AI-assisted software
delivery.

SWECore helps teams and serious individual builders review AI-assisted code
changes with visible scope, evidence, receipts, and known limits before the
change is trusted.

## What SWECore is designed to help with

These are design goals; the technical beta covers only the commands listed
under "What the technical beta does today".

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

## The review loop (target design)

This is the direction, not what the current build performs.

1. Scope the change.
2. Attach evidence.
3. Block unsupported claims.
4. Produce a reviewer-ready receipt.
5. Decide next action.

## What the technical beta does today

The current private build is an unsigned technical beta of a local command-line
tool for Linux and macOS. It is not a public release. It runs fully offline and
stores metadata only.

Does today:

- `swecore init`: set up repo-local `.swecore/` state and add it to `.gitignore`.
- `swecore doctor` and `swecore audit`: check that the local state and workspace
  lock are consistent and write a receipt. They do not inspect your code, your
  tests or an agent's behaviour.
- `swecore branch doctor`: read-only diagnosis of the local Git branch state.
- `swecore profile`: store a repo-local communication profile.
- `swecore setup codex --plan`: print a Codex MCP configuration plan.

Does not do yet: apply updates or rollbacks (`update`, `rollback`, `scope`
print `not_implemented` and exit non-zero), activate a licence, apply Codex
configuration for you, run or gate agent work, verify what changed, sign
packages, or support Windows.

See the [sample receipt](docs/sample-receipt.md) for real output and for the
target design the beta is heading towards.

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

SWECore is proprietary. See [LICENSE](LICENSE).

This public repository is provided for informational, evaluation, and product
showcase purposes only. It does not grant a license to the full commercial
runtime or any enterprise product surface.
