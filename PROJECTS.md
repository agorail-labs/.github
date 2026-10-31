# Agorail Labs — project scope and relationship

Agorail Labs hosts independently reviewed experiments in trustworthy commerce and payments infrastructure. Each repository owns its own specification, release decisions, test evidence, and readiness claims.

| Project | Scope | Current boundary |
| --- | --- | --- |
| [Subscription Change Quote (SCQ)](https://github.com/agorail-labs/subscription-change-quote) | A protocol-neutral lifecycle for quoting and committing **changes to existing subscriptions** across varied billing models. | v0.6.1 on main; v0.6.2 draft work under review. Experimental. Not a payment, payment-authorization, or subscription-creation protocol. |
| [Mutation Safety Envelope (MSE)](https://github.com/agorail-labs/mutation-safety-envelope) | Domain-blind constraints and outcome reporting for mutations to existing commercial state, including multi-unit admission and reconciliation. | v0.3.0 external-review candidate. Experimental. Does not define identity, payment authorization, settlement, or domain-specific resources. |

## Shared engineering questions

Both projects ask how a caller should reason about a proposed change **before** dispatch and interpret an observed outcome **afterward**. Recurring questions include quote drift, bounded acceptance, concurrent state changes, partial effects, unknown outcomes, retries, and independent evidence.

These similarities are **not** a declaration that SCQ implements MSE, that their guarantees are identical, or that one is a mandatory component of the other. Any integration must be specified, tested, and supported separately. Neither project inherits adoption, endorsement, or conformance claims from the other.

## Future directions

Payment-related authorization, transaction finality, refunds and reconciliation, and agent-initiated commerce are **areas for exploration**, not released Agorail capabilities. A new project should have an explicit scope and threat model before being presented as a protocol or implementation.

## Evidence principles

1. Distinguish direct live-provider observations from documentation-backed simulations, inferences, and unverified propositions.
2. Name the exact version, commit, and test conditions behind an assertion.
3. Record ambiguous or indeterminate execution as such; do not promote a successful API response to proof of the business effect.
4. Invite reproducible counterexamples and external review without describing review as adoption.
5. Treat payment processing, authorization, regulation, security, and production validation as distinct questions.

For actual behavior and limitations, consult the [SCQ evidence register](https://github.com/agorail-labs/subscription-change-quote/blob/main/research/EVIDENCE.md) and the [MSE falsification notes](https://github.com/agorail-labs/mutation-safety-envelope/blob/main/docs/falsification-notes.md).

## Institutional independence

Agorail Labs is independently maintained. It is not an official working group of UCP, ACP, or any payment or billing provider. References to external standards and companies do not imply sponsorship, certification, or endorsement.
