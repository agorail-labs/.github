<p align="center">
  <img src="../assets/agorail-mark.svg" alt="Agorail Labs logo" width="168" />
</p>

# Agorail Labs

**Safety contracts for AI-driven commerce changes.**

**Building the rails for trustworthy commerce.**

Agorail Labs is an independent, open-source initiative exploring how commerce and payments systems can make proposed changes, authorization boundaries, execution outcomes, and downstream effects **explicit, verifiable, and interoperable**.

We build experimental specifications, reference implementations, conformance tests, and reproducible evidence. Our emphasis is practical: a successful API response should not be mistaken for proof that the authorized business outcome occurred.

## Projects

| Project | Focus | Current maturity |
| --- | --- | --- |
| **[Subscription Change Quote (SCQ)](https://github.com/agorail-labs/subscription-change-quote)** | Quote → evaluate → commit → reconcile changes to existing subscriptions, including uncertainty about cost, timing, and final state. | Experimental v0.6.2 protocol; simulator-backed reference package **published on npm**: [`@agorail-labs/scq-reference@1.0.0-rc.2`](https://www.npmjs.com/package/@agorail-labs/scq-reference). Live-provider limitations disclosed in the repository. |
| **[Mutation Safety Envelope (MSE)](https://github.com/agorail-labs/mutation-safety-envelope)** | A domain-blind safety contract for mutations to existing commercial state: bounded acceptance, admission against live state, per-unit outcomes, and effect finality. | Experimental v0.4 admission and dependency reference package **published on npm**: [`@agorail-labs/mse-reference@1.0.0-rc.2`](https://www.npmjs.com/package/@agorail-labs/mse-reference). The repository source is a later, unreleased development revision — see the repository's "Two artifacts" note. |

Both projects are **research and external-review candidates**, not production-certified systems or adopted industry standards. Read each repository's security considerations, test coverage, and evidence limitations before relying on its claims.

## Watch the 92-second Agorail Demo

**Agorail: What Happens When an AI Agent Changes a Subscription?** — every output shown is a real run of the published packages against simulators, captured in a clean consumer project. Nothing in the video is a live provider observation.

https://github.com/user-attachments/assets/41968b11-403e-4999-bc59-5724fe5e642d

- [15-second silent preview](../assets/demo/agorail-preview-15s.mp4)
- [Narration transcript](../assets/demo/TRANSCRIPT.md)
- [**Run the example yourself → Try Agorail in Five Minutes**](https://github.com/agorail-labs/subscription-change-quote/blob/main/docs/TRY-AGORAIL-IN-FIVE-MINUTES.md)

*Experimental research software: MSE admission is not authorization, SCQ receipts are not provider execution guarantees, and no exactly-once or production-certified billing behavior is claimed. See each project's limitations before relying on any claim.*

## Start here — five minutes

One scenario runs through both projects: an AI agent is asked to raise a SaaS subscription from 100 to 120 seats, where the change requires a dependent add-on, changes recurring billing, and might time out after executing. The demonstrated path:

```text
proposed change ──► MSE admission ──► SCQ financial quote ──► separately authorized execution ──► receipt / reconciliation
                    (is the set        (what will it cost,      (the caller's own policy —       (what actually happened;
                     admissible?)       how strongly is          neither protocol grants         replay returns the receipt
                                        it guaranteed?)          authorization)                  instead of re-dispatching)
```

[**Try Agorail in Five Minutes**](https://github.com/agorail-labs/subscription-change-quote/blob/main/docs/TRY-AGORAIL-IN-FIVE-MINUTES.md) — install the two published packages in a clean project and run the whole sequence against a simulator. No billing credentials, no real provider.

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

1. Run [Try Agorail in Five Minutes](https://github.com/agorail-labs/subscription-change-quote/blob/main/docs/TRY-AGORAIL-IN-FIVE-MINUTES.md), then explore [SCQ](https://github.com/agorail-labs/subscription-change-quote) or [MSE](https://github.com/agorail-labs/mutation-safety-envelope) and review their stated limitations.
2. Use the project's GitHub Issues for reproducible defects or specific proposals — both repositories provide *Independent evaluation* and *Integration feedback* issue templates, and the joint [independent review package](https://github.com/agorail-labs/subscription-change-quote/blob/main/docs/INDEPENDENT-MSE-SCQ-REVIEW.md) lists falsification questions worth testing. Use Discussions where enabled for exploratory questions.
3. Read our [contribution guidelines](../CONTRIBUTING.md), [community expectations](../CODE_OF_CONDUCT.md), [security policy](../SECURITY.md), and [maintainership and decisions](../GOVERNANCE.md).

For help choosing a place to raise a question, see [support and contact paths](../SUPPORT.md).

## Independence and evidence

Agorail Labs is **not affiliated with, endorsed by, or speaking on behalf of** any payment provider, billing platform, standards consortium, or employer. References to UCP, ACP, Chargebee, Stripe, Paddle, Zuora, or other technologies are for technical research and interoperability discussion, not claims of certification or adoption. Provider-specific claims are qualified in each project's evidence records.

**Maintainer:** [@arjun2075](https://github.com/arjun2075). We welcome external collaboration; maintainership and project decisions are governed by the documented review process.

**Source:** [github.com/agorail-labs](https://github.com/agorail-labs) · **Project documents:** [scope and relationship](../PROJECTS.md)
