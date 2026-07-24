# Culture Note: Computational Context Drift and Jurisprudence

Status: proposed culture — revised after C challenge; pending Andie adjudication  
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

Both can produce different outcomes without any apparent change in governing policy.

From the standpoint of jurisprudence, the organization must be able to explain this fact:

> The same case, under the same apparent policy, produced a different result.

## Correction after challenge

The first draft proposed **decision environment** as a possible new durable object.

C's review materially corrected that hypothesis.

RFC-CDP-023 already defines most of the procedural relationship the draft was reaching for. Its **Decision Lifecycle Envelope** is a governed path index, explicitly not a warehouse, that references the decision's standing, recusal, Nemawashi, proposal admission, challenge, evidence, test, adjudication, legitimacy, execution, covenant, appeal, repair, and learning surfaces. Its governed path manifest and hash protect the integrity of those references.

The honest architectural conclusion is therefore:

> Do not create a second decision-environment object for procedural context. Extend the existing Decision Lifecycle Envelope where the existing governed path is incomplete.

The phrase **decision environment** may remain useful as ordinary-language description, but it is not presently justified as a new CDP primitive.

## Confirmed gap: computational context

The missing layer is the computational substrate that helped produce the result.

The reviewed CDP envelope and replay surfaces preserve who acted, under what authority, on which decision and governed records, with what result. They do not yet preserve first-class references for:

- model identity and version;
- model family or capability profile where relevant;
- harness or orchestration version;
- system-instruction or policy-bundle reference;
- tool-chain configuration;
- retrieval configuration and source set;
- memory or supplied-context reference;
- inference or execution constraints material to the result.

This is not merely software observability.

When a consequential result changes because the model, harness, tools, retrieval, or supplied context changed, the organization needs enough computational provenance to distinguish principled development from unexplained variance.

## Independence is not reproducibility

RFC-CDP-033 already identifies a related but different model risk: a model-generated proposal evaluated only by the same model family can create authority capture through participation.

That is an **independence and standing** problem.

This note addresses a different question:

> Did a change in the computational substrate alter the result, and can the organization explain that change?

A system can preserve independent review while failing computational reproducibility.

A system can also reproduce an output while failing independence, standing, legitimacy, or justice.

Neither problem should be allowed to hide inside the other.

## Drift, variance, and legitimate divergence

Not every changed outcome is drift.

A changed result may arise from:

- **evidence variance** — the facts, records, or available evidence changed;
- **policy or precedent variance** — the governing rule, interpretation, threshold, or precedent changed;
- **standing variance** — participation, recusal, or authority allocation changed;
- **procedural variance** — the governed path or lifecycle process changed;
- **computational variance** — the model, harness, tool chain, retrieval, memory, or execution configuration changed.

A further category must remain outside the drift taxonomy:

- **authority-pluralism divergence** — different, equally valid authorities reached different outcomes within their legitimate jurisdiction or sovereignty.

Under RFC-CDP-074, that divergence must not be mislabeled as unexplained drift or flattened into policy variance. The record should identify an Authority Conflict or authority-pluralism condition and preserve the distinct authority bases.

The purpose of the taxonomy is not classification for its own sake. It is to explain changed results without treating legitimate pluralism as defect.

## Proposed architectural seam

C identified two small changes that fit the existing architecture better than a new primitive.

### 1. Extend RFC-CDP-023 with computational context references

Add a `computational_context` reference family to the Decision Lifecycle Envelope in the same governed-reference style as existing stage and cross-plane hooks.

A candidate shape could include:

```yaml
computational_context:
  model_ref: <ref|null>
  harness_ref: <ref|null>
  system_instruction_ref: <ref|null>
  tool_chain_ref: <ref|null>
  retrieval_config_ref: <ref|null>
  memory_context_ref: <ref|null>
  execution_constraint_refs: [<ref>]
```

The envelope should index governed records rather than embed vendor-specific configuration.

These references should be included in the governed path manifest and protected by `governed_path_hash` whenever they are material to the decision.

The exact schema remains subject to challenge. In particular, CDP must decide which fields are required, conditional, nullable, or profile-specific.

### 2. Structure RFC-CDP-048 variance reporting

RFC-CDP-048 already contains the closest existing seed through `variance_summary` and `precedent_refs`.

Rather than creating a separate drift object, the Learn payload could structure variance through typed fields linked to governed records:

```yaml
variance:
  evidence_variance_refs: [<ref>]
  policy_precedent_variance_refs: [<ref>]
  standing_variance_refs: [<ref>]
  procedural_variance_refs: [<ref>]
  computational_variance_refs: [<ref>]
  authority_pluralism_condition: <none|claimed|confirmed|contested>
  authority_conflict_refs: [<ref>]
  unexplained_variance: <boolean>
  variance_summary: <string>
```

This keeps human-readable explanation while making the basis of changed outcomes inspectable and contestable.

## Replay and re-adjudication

The distinction between replay and re-adjudication remains useful, but should attach to the existing governed path.

### Replay

Replay asks:

> What can be reconstructed about the original result from the original governed path and computational context?

Replay serves historical reconstruction, audit, debugging, and reproducibility. It does not prove that the original decision was legitimate or correct.

Exact computational replay may be impossible when models, external tools, vendor services, or retrieval sources are unavailable. The obligation is to preserve the best available provenance and state clearly what cannot be reproduced.

### Re-adjudication

Re-adjudication asks:

> What result should be reached under the current governed path and computational context, and which typed variances explain any departure from the prior result?

Re-adjudication permits learning, changed evidence, changed law, better reasoning, legitimate authority pluralism, and repair. It must not silently overwrite the historical record.

Replay protects truth about what happened.

Re-adjudication protects the possibility of principled change.

## Consistency and jurisprudence

Consistency is not merely a product-quality preference.

For organizations making consequential decisions, similar cases should not diverge because a model was silently replaced, a harness changed, a retrieval source disappeared, or unrecorded discretion entered the process.

At the same time, absolute sameness can preserve error, injustice, and false jurisdictional uniformity.

The obligation is therefore:

> consistent treatment, plus a visible and contestable account of principled departure, legitimate authority pluralism, and unresolved variance.

Software versioning is evidence. It is not justification.

Reproducibility is evidence. It is not legitimacy.

## Recommended next move

Do not promote **decision environment** as a new primitive.

Prepare a bounded two-RFC proposal for Andie's adjudication:

1. add computational-context reference hooks to RFC-CDP-023 and include material references in the governed path manifest;
2. replace or supplement RFC-CDP-048's free-text variance summary with typed variance and authority-pluralism fields.

Before implementation, reconcile the proposed record types and references with RFC-CDP-021, RFC-CDP-022, RFC-CDP-033, RFC-CDP-047, RFC-CDP-048, RFC-CDP-061, and RFC-CDP-074.

## Separate integrity finding

C also identified a live reference-integrity issue: the files currently located at the renumbered RFC-CDP-047 and RFC-CDP-048 paths reportedly retain legacy internal headers naming RFC-CDP-008 and RFC-CDP-009.

That issue is separate from computational context, but it resembles the silent-reference-mutation failure mode named by RFC-CDP-023. It should be verified and repaired through a separate, narrow change rather than folded into this proposal.

## Guardrails

- Do not duplicate the Decision Lifecycle Envelope under a new name.
- Do not equate computational provenance with legitimacy.
- Do not treat replay as proof that an earlier decision was correct.
- Do not treat changed model output as principled precedent development by itself.
- Do not freeze unjust precedent merely to maximize consistency.
- Do not label legitimate sovereignty-based divergence as drift.
- Do not let authority capture and computational variance blur into one problem.
- Do not pretend exact replay is always technically possible.
- Do not embed large vendor-specific runtime payloads inside the lifecycle envelope.
- Do not canonize the variance taxonomy before RFC-level challenge and adjudication.

## Pillow fort formulation

The room does not need a second map of the road it already traveled.

It needs the existing map to remember which engine, instruments, guides, and sources helped carry the decision—and to say plainly when a different sovereign road was never drift at all.