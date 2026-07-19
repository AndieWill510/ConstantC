# Culture Note: Cognitive Load as Governance

Status: proposed culture — pending challenge and adjudication  
Date: 2026-07-18  
Steward: Andie  
Room: ConstantC  
Privacy: public-safe

---

## Opening principle

Human attention is a governed resource.

A system can fail even when every agent is individually helpful if the combined output places the human steward under an unbounded pile of dense technical detail, unresolved decisions, duplicated explanations, and competing next actions.

That is not merely a usability problem. It is a governance problem.

## Why this matters

ConstantC exists because no participant should have to carry the whole room in private memory, reconstructive stamina, or hidden context.

Agent-assisted work can accidentally rebuild the same harm at a higher speed. If Codex, Claude, G, Dispatch, CI, and future agents all send complete internal monologues to Andie, the room may increase information while decreasing usable judgment.

Availability of information is not the same thing as access. More output is not automatically more witness. More detail is not automatically more care.

## Core distinction

Cognitive load governance does not mean hiding material that matters.

It means routing information according to the role, decision, and moment.

- **Status** tells the room where the work stands.
- **Evidence** tells the room what was tested or observed.
- **Decision requests** tell the human steward what requires judgment.
- **Implementation detail** supports review when review is the task.
- **Archive detail** preserves recoverability without forcing immediate ingestion.

A healthy workflow does not make Andie read archive detail when the next legitimate move is one decision.

## Room rule

By default, agent systems should report:

1. what changed;
2. whether validation passed;
3. what remains unresolved;
4. whether human judgment is needed;
5. the smallest next action.

Dense implementation detail should appear when requested, when needed for review, or when withholding it would hide a risk.

The default interface should be legible enough for a tired human to remain a legitimate participant.

## Human attention limits

When Dispatch or another routing layer assigns work, the packet should be able to state human attention limits.

Examples:

- summarize in five bullets before giving detail;
- ask at most one decision question at a time;
- separate blocking risks from optional refinements;
- do not include full logs unless requested;
- link to raw evidence instead of pasting it into the decision surface;
- state whether the human can safely ignore the message until review time.

These limits are not indulgences. They are part of preserving the steward's ability to adjudicate.

## PRs as cognitive-load architecture

Pull requests are not only code review surfaces. They are memory and pacing surfaces.

A good PR lets the human steward review the durable artifact instead of holding an entire chat cascade in working memory.

For agent-assisted work, a PR should separate:

- summary;
- scope;
- provenance;
- tests / validation;
- review findings;
- requested decisions;
- unresolved risks;
- raw details or logs.

When this separation is done well, the human can move between overview and detail without being forced to absorb everything at once.

## Anti-flooding rule

Do not make the human steward become the integration bus for unbounded agent output.

If several agents produce findings, the workflow should consolidate them into a review surface that preserves source, role, and evidence while reducing duplicated or competing demand on human attention.

A flood of accurate details can still be an access failure.

## Relationship to provenance

This note was split from `culture/agent-provenance-and-role-separation.md` after C's review.

The provenance note keeps the identity, role, authority, and action separation. This note carries the broader attention-governance principle: systems should preserve the human steward's ability to remain present, discerning, and legitimate in the workflow.

A provenance packet that records who acted but overwhelms the human reviewer has preserved auditability while damaging adjudication.

Both matter.

## Guardrails

When this principle is used, preserve these boundaries:

- Do not hide blocking risks to make a summary feel clean.
- Do not infantilize the human receiving cognitive-load support.
- Do not confuse brevity with honesty.
- Do not make all detail disappear; preserve it where it can be retrieved.
- Do not require distress, disability disclosure, or exhaustion before using humane defaults.
- Do not let agent politeness become information flooding in softer language.
- Do not treat human overwhelm as proof that the human is not technical enough.
- Do not turn cognitive-load governance into overcontrol; the human may still ask for full detail.

## Pillow fort formulation

No one should have to stand under the whole waterfall to prove they are allowed to drink.

Give the room cups, channels, pools, and valves.
