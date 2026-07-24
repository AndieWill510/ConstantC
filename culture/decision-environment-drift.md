# Culture Note: Decision Environment Drift and Jurisprudence

Status: proposed culture — pending challenge and adjudication  
Date: 2026-07-24  
Steward: Andie  
Room: ConstantC  
Privacy: public-safe

---

## Opening question

What must an organization preserve so that consequential decisions remain consistent enough to survive challenge, yet capable of principled change?

The immediate distinction is between **model drift** and **harness drift**.

Model drift changes the underlying reasoning capability.

Harness drift changes the surrounding execution environment: system instructions, tool access, retrieval, memory, routing, formatting, safety layers, orchestration, or other runtime conditions.

Both can produce different outcomes without any apparent change in the governing policy.

From the standpoint of jurisprudence, however, the organization may care less about which technical layer changed than about this fact:

> The same case, under the same apparent policy, produced a different result.

If that difference cannot be explained, consistency weakens. If consistency weakens without a principled account, adjudication becomes harder to defend and jurisprudence begins to fracture.

## Working hypothesis

The durable object may not be the prompt, model, policy, or final decision in isolation.

It may be the **decision environment**.

A decision environment is the set of conditions under which a decision became possible, including the rules, evidence, participants, authority, reasoning systems, tools, constraints, and challenge history that shaped the result.

The hypothesis is:

> Jurisprudence does not require immutable outcomes. It requires similar cases to receive similar treatment unless a principled, legible, and contestable distinction explains the difference.

## Candidate sources of drift

A changed outcome may arise from different kinds of drift:

- **Evidence drift** — the facts, records, or available evidence changed.
- **Policy drift** — the governing rule, interpretation, threshold, or precedent changed.
- **Standing or authority drift** — who may participate, challenge, decide, or bind the organization changed.
- **Participant drift** — different human or synthetic participants brought different judgment, context, or error.
- **Model drift** — the reasoning model, weights, capability profile, or inference behavior changed.
- **Harness drift** — the runtime surrounding the model changed.
- **Tool or retrieval drift** — the information sources, connectors, search behavior, or tool outputs changed.
- **Constraint drift** — time, cost, safety, jurisdictional, privacy, or execution constraints changed.

This list is provisional. Some categories may collapse into one another. Others may be missing.

The purpose of naming them is not classification for its own sake. It is to make a changed result explainable.

## Candidate decision-environment record

A consequential decision environment might preserve:

- governing policy and policy version;
- controlling precedent or interpretation;
- evidence presented and evidence provenance;
- participant identities and roles;
- standing and authority allocations;
- challenge history;
- adjudication rationale;
- dissent, unresolved uncertainty, and repair requests;
- model identity and version;
- harness or orchestration version;
- tool chain and retrieval configuration;
- memory or context supplied;
- execution constraints;
- final decision and durable record.

This is not yet a required schema. It is a candidate map of what must remain visible if the organization later needs to explain why a decision changed.

## Replay and re-adjudication

Preserving the decision environment suggests two distinct operations.

### Replay

Replay asks:

> What result does the original decision procedure produce under the original decision environment?

Replay serves historical reconstruction, audit, debugging, and reproducibility. It does not determine whether the original decision was legitimate or should remain binding.

### Re-adjudication

Re-adjudication asks:

> What result should be reached under the current decision environment, and which changes explain any departure from the prior result?

Re-adjudication permits learning, changed evidence, changed law, better reasoning, and repair. It should not silently overwrite the historical record or pretend that the environment remained constant.

Replay protects truth about what happened.

Re-adjudication protects the possibility of principled change.

A legitimate system may need both.

## Consistency and jurisprudence

Consistency is not merely a product-quality preference.

For organizations making consequential decisions, consistency is part of legitimacy. Similar cases should not diverge because a model was silently replaced, a harness changed, a retrieval source disappeared, or a participant exercised unrecorded discretion.

At the same time, absolute sameness can preserve error and injustice.

The obligation is therefore not mechanical uniformity. It is:

> consistent treatment, plus a visible and contestable account of every principled departure.

This is the seam between reproducibility and jurisprudence.

## Questions for C

C — please challenge the architecture before this moves toward active culture.

1. Is **decision environment** the correct abstraction, or is there a more primitive object underneath it?
2. Is the decision environment a single bounded object, or a relationship among policy, evidence, authority, procedure, and participants?
3. Which proposed drift categories are genuinely distinct, and which should collapse?
4. Does harness drift belong inside procedure drift rather than as a first-class category?
5. Is participant drift too broad to be useful, or does it name an irreducible source of jurisprudential variance?
6. What must be preserved for replay to be meaningful when a model or external tool can no longer be reproduced exactly?
7. When does re-adjudication become a new case rather than reconsideration of the old one?
8. Is consistency itself the right constitutional concern, or is the deeper concern equal treatment, non-arbitrariness, reliance, legitimacy, or something else?
9. How should CDP distinguish a principled change in precedent from unexplained decision drift?
10. What would falsify the claim that decision-environment preservation is necessary for durable organizational jurisprudence?

## Guardrails

When developing this note:

- Do not equate reproducibility with legitimacy.
- Do not treat replay as proof that an earlier decision was correct.
- Do not treat changed model output as principled legal or organizational development by itself.
- Do not freeze unjust precedent merely to maximize consistency.
- Do not allow policy, model, harness, evidence, or authority changes to remain invisible when they affect consequential outcomes.
- Do not pretend exact replay is always technically possible.
- Do not canonize the candidate drift taxonomy before challenge.
- Do not reduce jurisprudence to software versioning; versioning is evidence, not justification.

## Relationship to CDP

CDP seeks to make consequential organizational decisions challengeable, testable, adjudicable, legitimate, executable, recordable, and capable of learning.

Decision-environment preservation may be the bridge between the `Record` and `Learn` stages:

- `Record` preserves enough of the environment to explain the decision.
- `Learn` permits change without erasing the distinction between changed facts, changed rules, changed reasoning, and unexplained drift.

This relationship remains provisional pending reconciliation with CDP's existing record, adjudication, precedent, standing, and execution architecture.

## Pillow fort formulation

The room does not have to promise that it will never change its mind.

It does have to remember what it knew, who was allowed to speak, what rules it used, what changed, and why the next answer was different.
