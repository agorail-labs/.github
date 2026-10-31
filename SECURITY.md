# Security reporting — Agorail Labs

Agorail Labs' current projects are experimental specifications and reference implementations. They are **not production-hardened payment or authorization systems**. No security-support lifecycle or fixed response SLA is offered.

## Report a potential vulnerability privately

If the affected repository offers GitHub **Private vulnerability reporting**, use **Security → Report a vulnerability** for that repository.

Otherwise, use a private contact channel listed on the applicable repository maintainer's GitHub profile. **Do not** publish exploit instructions, secrets, private customer details, credentials, or other sensitive information in a public issue or discussion. Public GitHub issues are not confidential.

A useful report identifies the affected project and version/commit, a minimal sanitized reproduction, the violated invariant, possible impact, and any mitigating conditions.

## Examples of relevant problems

- A quote or acceptance constraint bypass that permits materially different effects.
- An unauthorized, stale, wrong-target, or wrong-unit mutation.
- A retry or recovery path that incorrectly treats an unknown execution outcome as definitely safe.
- Inconsistent receipt, reconciliation, or evidence records that conceal an actual effect.
- Exposed credentials or sensitive information in reference implementations.

A simulator finding is **not evidence** of a security defect in a named billing or payment provider. Production integrations need independent threat modeling, authorization controls, live-provider validation, and security review.

Repository-specific security policies take precedence. In particular, see [SCQ's security policy](https://github.com/agorail-labs/subscription-change-quote/blob/main/SECURITY.md). Non-sensitive documentation and correctness issues may be filed in the relevant repository's Issues.
