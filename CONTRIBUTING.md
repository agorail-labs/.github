# Contributing to Agorail Labs

Agorail Labs develops open-source research, specifications, conformance work, and reference implementations for commerce and payments infrastructure. We welcome **specific, reproducible criticism** as well as fixes and new ideas.

## Choose a repository

- **[SCQ](https://github.com/agorail-labs/subscription-change-quote)** — quote/commit/reconcile changes to existing subscriptions.
- **[MSE](https://github.com/agorail-labs/mutation-safety-envelope)** — domain-blind mutation safety and multi-unit outcomes.

Read the relevant repository's README, specification, evidence register, and existing contribution guidance first. Repository-specific policies take precedence over this organization default.

## Good contributions

- A minimal reproduction of a correctness, security-boundary, or conformance defect.
- A concrete example or counterexample that tests an assumption.
- Tests that distinguish known outcomes from uncertainty and failure.
- Documentation corrections with traceable evidence.
- A focused protocol or adapter proposal with precise semantics, limitations, and failure behavior.

Use **Issues** for concrete, actionable findings and **Discussions**, when available, for open-ended architecture or integration questions. For meaningful behavior or normative changes, open an issue before implementing a broad redesign. A discussion, issue, or PR does not confer approval.

## Evidence and technical review

Describe the affected version/commit, steps to reproduce, expected and observed behavior, and proof supporting any claim. Separate direct API observation from provider documentation, simulations, inference, and open questions. Never assert a third-party provider has a vulnerability or supports a behavior based solely on simulator output.

Proposals changing a safety invariant should explain scope, compatibility effects, negative cases, state races, partial application, unknown outcomes, and recovery. Keep documentation, code, schemas, tests, and examples in agreement; run the repository's documented validations.

## Contributions and attribution

Contributions remain attributable to their authors through Git history and GitHub review. Maintainers decide whether and when changes are merged; authorship or participation does not automatically convey maintainer authority, endorsement, or a release commitment.

Never share credentials, sensitive customer information, or non-public provider data. Use the applicable [security reporting path](SECURITY.md) for confidential vulnerabilities. Follow our [code of conduct](CODE_OF_CONDUCT.md).
