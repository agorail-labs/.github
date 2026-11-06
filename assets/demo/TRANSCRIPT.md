# Narration transcript — "Agorail: What Happens When an AI Agent Changes a Subscription?"

Full video: [`agorail-demo-90s.mp4`](agorail-demo-90s.mp4) (92.0 s, 1920×1080, narrated).
Voice: synthesized (Helio), English. Captions: [`captions.vtt`](captions.vtt)
(15 cues, timed from the actual segment durations).

## 00:00–00:15 — The problem

An AI agent is told: increase our subscription from one hundred to
one hundred twenty seats. Simple, until three things go wrong: a
required dependency is missing, the financial consequences are
unclear, and the execution itself is uncertain.

## 00:15–00:37 — MSE admission

The agent proposes the seat increase, but the required analytics
entitlement is missing from the change. MSE evaluates the whole set,
read-only, before anything is dispatched, and refuses it, with a
witness naming the missing add-on. Include the add-on, and the
complete change passes admission. Admission is not authorization: it
judges completeness, never permission.

## 00:37–01:01 — SCQ financial quote

Next, SCQ quotes the financial consequences before any mutation: an
immediate effect of two hundred dollars, and a resulting recurring
amount of twelve hundred dollars, each marked determined, not
guessed. A separate approval policy, the caller's own code, not the
protocol, accepts the quote. The change commits against the
simulator, and the receipt records: committed, reconciliation OK.

## 01:01–01:21 — Recovery safety

After a restart, re-executing the same intent does not dispatch
again: the durable coordinator replays the recorded receipt. One
dispatch, start to finish. A lost provider response is a different
case: the outcome is indeterminate, retry is refused, and
reconciliation happens by observation, never by blind re-dispatch.

## 01:21–01:32 — Call to action

Try Agorail in five minutes. The packages are on npm, and the
quickstart needs no billing credentials. Agorail is experimental
research software: no production billing certification is claimed.
