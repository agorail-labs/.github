<p align="center">
  <img src="../assets/agorail-mark.svg" alt="Agorail Labs logo" width="168" />
</p>

# Agorail Labs

**Building the rails for trustworthy commerce.**

Agorail Labs is an independent, open-source initiative exploring how commerce and payments systems can make proposed changes, authorization boundaries, execution outcomes, and downstream effects **explicit, verifiable, and interoperable**.

We build experimental specifications, reference implementations, conformance tests, and reproducible evidence. Our emphasis is practical: a successful API response should not be mistaken for proof that the authorized business outcome occurred.

## Projects

| Project | Focus | Current maturity |
| --- | --- | --- |
| **[Subscription Change Quote (SCQ)](https://github.com/agorail-labs/subscription-change-quote)** | Quote → evaluate → commit → reconcile changes to existing subscriptions, including uncertainty about cost, timing, and final state. | Experimental v0.6.2 protocol and simulator-backed reference package; release configuration prepared, with live-provider limitations disclosed. |
| **[Mutation Safety Envelope (MSE)](https://github.com/agorail-labs/mutation-safety-envelope)** | A domain-blind safety contract for mutations to existing commercial state: bounded acceptance, admission against live state, per-unit outcomes, and effect finality. | Experimental v0.4 admission and dependency reference implementation; npm packaging prepared, with runtime guarantees limited to the stated model. |

Both projects are **research and external-review candidates**, not production-certified systems or adopted industry standards. Read each repository's security considerations, test coverage, and evidence limitations before relying on its claims.

### How the projects relate

SCQ addresses a **specific business domain**: changes to existing subscriptions across heterogeneous billing providers. MSE studies the **general safety boundary** for changes to commercial state across domains such as retail, travel, subscriptions, and contracts.

Their protocols remain **separate specifications**, but a [simulator-only MSE–SCQ integration](https://github.com/agorail-labs/subscription-change-quote/pull/57) now runs in cross-repository Node 20/22 CI. MSE performs read-only dependency admission; SCQ validates subscription-specific commercial effects and provides durable dispatch exclusion; a separate experimental bridge binds repeated quotes to one approved business intent. The demonstrated workflow includes a seat-change/addon dependency, replay after a fresh quote, failure-before-dispatch, and mock multi-unit outcomes. This is **not** provider-certified execution, general multi-unit atomicity, or proof of provider-side exactly-once effects. Both packages may be adopted independently; the bridge remains experimental. See [project scope and relationship](../PROJECTS.md).

## Areas of work

- **Commerce protocols:** express proposed transactions and modifications with explicit business semantics.
- **Payments and authorization:** investigate consent-to-execution boundaries, payment-related state, and verifiable outcomes. *This is a future area of exploration, not a claim of a shipped payments protocol.*
- **Mutation safety:** surface drift, partial application, unknown outcomes, and safe recovery paths.
- **Interoperability and conformance:** test assumptions and record what real systems do, without turning simulations into deployment claims.

## Get involved

We welcome independent technical criticism, counterexamples, tests, architecture discussion, and evidence from real integrations **when it can be shared responsibly**.

1. Explore [SCQ](https://github.com/agorail-labs/subscription-change-quote) or [MSE](https://github.com/agorail-labs/mutation-safety-envelope) and review their stated limitations.
2. Use the project's GitHub Issues for reproducible defects or specific proposals. Use Discussions where enabled for exploratory questions.
3. Read our [contribution guidelines](../CONTRIBUTING.md), [community expectations](../CODE_OF_CONDUCT.md), [security policy](../SECURITY.md), and [maintainership and decisions](../GOVERNANCE.md).

For help choosing a place to raise a question, see [support and contact paths](../SUPPORT.md).

## Independence and evidence

Agorail Labs is **not affiliated with, endorsed by, or speaking on behalf of** any payment provider, billing platform, standards consortium, or employer. References to UCP, ACP, Chargebee, Stripe, Paddle, Zuora, or other technologies are for technical research and interoperability discussion, not claims of certification or adoption. Provider-specific claims are qualified in each project's evidence records.

**Maintainer:** [@arjun2075](https://github.com/arjun2075). We welcome external collaboration; maintainership and project decisions are governed by the documented review process.

**Source:** [github.com/agorail-labs](https://github.com/agorail-labs) · **Project documents:** [scope and relationship](../PROJECTS.md)
