# Trust Boundary

## Current posture

SWECore is in early access. Public materials should explain the intended trust
model while avoiding production, security, compliance, or enterprise readiness
claims.

## Local-first by design

SWECore is positioned as local-first: governance, receipts, and review context
are intended to stay close to the repository workflow.

## BYOK-oriented

SWECore is BYOK-oriented. Teams should be able to use their own approved AI
providers and development environments rather than depending on a single bundled
model provider.

## No silent mutation

SWECore should not silently change code, configuration, production services, or
remote systems. Review and consent boundaries matter.

## Review before change

The workflow should make scope, evidence, limits, and reviewer next steps
visible before a change is trusted.

## Workflow receipts

Receipts are meant to separate:

- what changed;
- what evidence exists;
- what is still limited;
- what should happen next.

## Consent-based telemetry

Any telemetry posture should be consent-based. Public wording should not imply
unreviewed upload of code, prompts, secrets, or private repository content.

## What the waitlist asks

The early-access waitlist may ask for low-sensitivity information such as:

- name and email;
- role or company/team-size bucket;
- current AI coding tools;
- preferred operating system or development environment.

## What the waitlist does not ask

The waitlist should not ask for:

- private repository URLs;
- source code;
- API keys, secrets, or access tokens;
- customer data;
- production logs;
- GitHub, IDE, or model-provider account access.

## What is not claimed today

SWECore does not currently claim production readiness, security certification,
compliance certification, hosted dashboard availability, enterprise control
plane availability, immutable audit, automatic delivery validation, or full
runtime parity.
