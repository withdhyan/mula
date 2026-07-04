# Mūla: a sovereign wallet for human values

**Whitepaper v0.1 — architecture and research grounding.** Status: design + working MVP scaffold; honest about what's built vs. planned. 2026-07-04, Holon Research.

## 1. The problem: profiled for everyone but yourself

Recommender systems hold the most consequential model of you that exists — and every one of them is optimized for someone else's objective: engagement, conversion, retention. The result is a structural absurdity: the systems that know you best are constitutionally incapable of being on your side. Meanwhile the one dataset that would let an AI genuinely act in your interest — what you actually value, in your own words — exists nowhere, because nobody will hand it to an engagement machine, and they're right not to.

## 2. The thesis: meaning-maxxing

We take the opposite objective. **Meaning-maxxing** is our term for AI built to maximize meaning rather than engagement or productivity: an agent whose north star is what makes your life feel worth living by *your* articulation, not your click-through rate. That requires two things nobody has combined: a rigorous way to elicit values (not personality quizzes), and an architecture where the resulting data is structurally incapable of being used against you.

## 3. Value cards: the data model

A value card is a short, specific, arguable artifact:

> **Let them feel the small failures** · *When my kid struggles* — noticing my urge to rush in, and asking whether this fall is one of the ones that teaches.

Cards have a context ("when my kid struggles"), attentional policies (what you actually attend to when choosing well), and the owner's explicit endorsement. This follows the Meaning Alignment Institute's published **Moral Graph Elicitation** research [1, 2]: values elicited as attentional policies anchored in real past choices resist both survey-answer aspiration and horoscope vagueness. Our elicitation is tiered by depth — a 90-second forced-choice deck ("which is more you," never yes/no, because people endorse any flattering generic statement), an agent-drafted flow grounded in observed behavior, and a full interview. Depth is always the user's choice.

Three integrity rules, absolute: nothing becomes a card without per-card explicit endorsement; a tossed draft is hard-deleted (verified by test, not policy); cards drafted by an agent are hypotheses until the human signs them.

## 4. Sovereignty architecture: crypto enters where trust exits

The design principle for the entire stack: **cryptography is adopted exactly where trust runs out, and nowhere before.**

- **Today (single operator):** card content encrypted at rest at the field level — ciphertext even to the operator's database. Consent as four separate, versioned, logged events (account / elicitation with explicit sensitive-category consent / any future use / research — never bundled). Export and full deletion as one-tap user actions; breach disclosure committed at 72 hours. Sensitive processing follows a sovereign-lane pattern: the most personal context routed only to zero-data-retention model endpoints.
- **As trust boundaries appear:** user-held keys signing endorsed cards (a card becomes unforgeable and portable); selective disclosure so a single card can be proven without opening the wallet [5]; private set intersection so two agents can discover common ground without either revealing its contents [3, 4]; transformed embeddings that preserve utility while killing invertibility [6].
- **Never:** a token, a chain with user content, advertising, or data resale. These are not roadmap decisions; they are constitutional.

## 5. Epistemic posture: pre-registered, built in public

Claims about what value-data can do should be tested like science, not marketed like features. We pre-registered our next step — hypothesis, method, kill criteria — before running it, hash-stamped (`ddbe9cd`) and sealed until the results are in; the readout publishes pass or fail. The company itself runs in public on an open-source agent stack, and this whitepaper will be revised in the open as reality corrects it.

## 6. What Mūla is not (yet)

The wallet is the product. Where it goes next — what becomes possible between two people who each hold a wallet — is the sealed experiment above, and we've committed not to claim it before the evidence exists. Watch the readout.

## References

[1] Meaning Alignment Institute — Moral Graph Elicitation: values as attentional policies, moral graphs from attested wisdom transitions (published MGE research; meaningalignment.org).
[2] "Full-Stack Alignment" — arXiv:2512.03399 (value stewardship agents; the research agenda this work applies in the field).
[3] Son et al., fuzzy PSI over cosine similarity (FPHE) — IACR ePrint 2025/054.
[4] van Baarsen & Pu, VOLE-based fuzzy PSI — IACR ePrint 2025/911.
[5] BBS+ selective disclosure signatures — IETF/W3C verifiable credentials family.
[6] STEER: similarity-preserving, inversion-resistant embedding transforms — arXiv:2507.18518.

*v0.1 — expect revisions in public. Corrections welcome: the repo takes issues.*
