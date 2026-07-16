# Worked Case: Standing and Epistemic Safety in AI-Assisted Prior Authorization

Status: Proposed worked case  
Date: 2026-07-15  
Last revised: 2026-07-15  
Steward: Andie  
Room: ConstantC  
Related files: `culture/standing-is-the-first-covenant.md`, `culture/standing-vs-epistemic-safety.md`, `culture/epistemic-safety.md`, `canon/unlost-systems-principles.md`, `canon/c-epistemic-boundary.md`, `canon/grief-and-evidence-boundary.md`

---

## Why this case exists

This case tests three different failures that were previously blurred together:

- **standing-allocation failure:** the beneficiary is not recognized as a relevant source within a domain where her contribution should matter;
- **epistemic-safety failure:** policy recognizes her as a source, but practice structurally discounts her contribution;
- **contestability failure:** no legitimate mechanism exists to challenge or reweigh the decision.

The case also tests whether a formally named path is reachable in practice.

---

## Bounded policy context

Beginning in 2026, the Centers for Medicare & Medicaid Services began testing the Wasteful and Inappropriate Service Reduction, or WISeR, model in six states for selected services under Original Medicare.

WISeR uses enhanced technology, including AI and machine learning, to support prior-authorization review. Licensed clinicians make final adverse determinations, and existing appeal rights remain available.

WISeR's current intake is provider- or supplier-submitted. The beneficiary narratives below are a constructed governance hypothetical, not a claim about WISeR's exact present intake mechanics.

This case does not claim that Medicaid has been nationalized or that state authority has been categorically displaced. Medicare is federally administered; Medicaid remains a federal-state program.

The narrower claim is enough:

> A federally governed, AI-assisted prior-authorization process can preserve formal appeal rights while denying an affected beneficiary meaningful participation in the controlling inquiry.

Public context:

- https://www.cms.gov/priorities/innovation/innovation-models/wiser
- https://time.com/7313351/medicare-prior-authorization-pilot-states-concerns/
- https://www.kiplinger.com/retirement/medicare/prior-authorization-coming-to-traditional-medicare

The sources establish policy context, not the hypothetical discrimination pattern below.

---

## The system

Imagine a CDP-governed public-health prior-authorization system.

It is legible. Every denial is explained. Provenance, policy version, model version, reviewer identity, and evidence source are recorded. Requests can be appealed. Human reviewers remain available. Disability accommodations are offered. Narrative evidence and case-specific context can be submitted. A licensed clinician makes the final adverse determination.

By conventional governance measures, the system appears exemplary.

---

## Case 1: standing allocated and epistemic safety present

The beneficiary is recognized by policy as a relevant source concerning:

- lived effects and functional impairment;
- chronology and treatment response;
- preferences and consent;
- communication needs;
- and errors in how her account is represented.

Her account is understood with effective accommodation. Credibility is assessed through evidence quality rather than disability, distress, fluency, or communication style. Material correction can revise the controlling account. Reasons are recorded. Review and reopening conditions are known.

Standing is allocated and realized.

---

## Case 2: standing allocated and epistemic safety absent

An autistic beneficiary seeks authorization for a covered treatment.

Policy formally recognizes her lived account as relevant. She submits pain, sensory consequences, executive-function loss, chronology, and the effects of delayed treatment. Her physician supplies supporting clinical evidence.

The appeal channel functions. Everything enters the record. A human reviewer reads it.

Yet her own account is consistently assigned low weight because it is treated as nonlinear, emotionally excessive, insufficiently clinical, internally inconsistent, or unreliable by category.

A materially similar beneficiary presents the same facts through language the model and reviewer recognize as orderly, calm, and medically authoritative. The second appeal succeeds.

The policy allocation did not change.

The realization did.

This is an epistemic-safety failure: standing exists de jure but does not survive contact with practice.

---

## Case 3: standing absent despite a formal appeal channel

The system accepts appeals and multiple evidence categories. It accepts clinician evidence, institutional records, structured measurements, legal argument, and beneficiary documents.

But the governing participant-role map declares that beneficiary testimony is relevant only as supporting material authenticated and interpreted by a clinician. The beneficiary cannot directly correct how her lived effects, chronology, preferences, or communication are represented.

The appeal mechanism is broad in form, but the beneficiary is not recognized as a source within a domain where she should matter.

The standing failure is not simply that she lacks an upload field. The mechanism may accept her document.

The failure is that the constitutional allocation defines her contribution as incapable of independently revising the account.

A complete contestability discipline may eventually treat this as a defective evidence-category or participant-role rule. If every case of this kind can be fully repaired within contestability, standing weakens from primitive to sub-clause. That remains a live falsification path.

---

## Case 4: contestability absent

The beneficiary cannot challenge the model-supported interpretation, credibility discount, factual record, policy application, or reviewer decision through a legitimate reweighing mechanism.

This is a contestability failure regardless of whether the institution nominally recognizes the beneficiary as a source.

Standing without a mechanism is ceremonial.

---

## The operational distinctions

Standing asks:

> Within what domain is this participant entitled to matter?

Epistemic safety asks:

> Is that entitlement honored in actual understanding, credibility weighting, adjudication, and repair?

Contestability asks:

> Through what legitimate mechanism can the account or decision be challenged and reweighed?

From outcome data alone, standing-allocation and epistemic-safety failures may look identical.

They can be distinguished only by independently examining:

- policy and participant-role definitions;
- formally accepted evidence categories;
- actual credibility rationales;
- process traces;
- and outcome patterns.

---

## Sufficient, not identical standing

Standing does not equalize authority.

- The beneficiary has standing concerning lived effects, chronology, preferences, consent, communication needs, and representation errors.
- The treating clinician has standing concerning diagnosis, medical necessity, treatment history, prognosis, and clinical risk.
- The reviewing clinician has adjudicative authority bounded by policy, evidence, conflicts, and reviewability.
- The model has consequential force but no independent moral standing or unreviewable authority.
- The agency has policy authority but cannot treat its own records as infallible.
- The public has standing concerning lawful expenditure, equity, aggregate outcomes, and incentive effects.

For each participant, the system must name:

1. relevant domain;
2. entry mechanism;
3. revision condition;
4. rejecting authority and required reasons;
5. review and reopening path;
6. evidence that the path is reachable.

If the sixth element is missing, sufficient standing remains rhetoric.

---

## Reachability audit

A policy path may exist while remaining structurally unusable.

The audit should therefore test:

- appeal reversal rates by disability, language, communication style, source role, and access to representation;
- materially similar cases with different source identities or presentation styles;
- stated versus actual credibility rationales;
- abandonment and time-to-resolution rates;
- whether accommodations change comprehension and outcomes;
- whether new beneficiary evidence changes decisions at plausible rates;
- whether successful challenges repair downstream records and model inputs;
- and whether the threshold for revision is realistically available to the participant.

The question is not merely whether the door exists.

It is whether the affected person can reach and open it.

---

## Consent

Prior authorization is not an ordinary consensual inquiry. A beneficiary cannot simply decline without risking coverage or care.

Where refusal is not realistic, legitimacy requires meaningful disclosure and representation:

- that automated tools are materially involved;
- what role they play;
- what data and testimony are used;
- how credibility and medical necessity are evaluated;
- who decides;
- what correction, accommodation, representation, review, and appeal rights exist;
- what downstream records may be affected;
- and how successful challenge repairs outcome and record.

Consent without standing is formality.

Standing without disclosure is blind participation.

---

## CDP implementation seam

Standing determination belongs inside the existing CDP cycle rather than a new ninth stage.

### Propose

Record treatment requested, rule invoked, model recommendation, evidence by source, communication needs, uncertainty, and participant-role map.

### Challenge

Permit challenges to factual accuracy, policy application, model interpretation, credibility discounts, standing allocation, missing context, and inaccessible procedure.

### Test

Compare materially similar cases. Test whether identity, disability, distress, fluency, language, or communication style alters credibility or outcomes after relevant differences are controlled. Test whether each named revision path is reachable.

### Adjudicate

Name the authority, conflicts, evidence standard, participant domains, credibility rationale, standing allocation, and what would have changed the result.

### Legitimize

Confirm lawful authority, sufficient standing, effective accommodations, known standards, bounded closure, and independent-review triggers for consequential standing disputes.

### Execute

Approve, deny, modify, or request additional information; communicate accessibly; prevent unsafe execution while a timely high-stakes challenge remains unresolved where law permits.

### Record

Preserve evidence, provenance, credibility rationales, standing determinations, uncertainty, model and policy versions, reviewer identity, and incentives.

### Learn and repair

Repair immediate and downstream records. Measure reversal, delay, abandonment, and harm. Revise policy, model, workflow, and training when patterned failures recur.

CDP does not manufacture standing by creating more procedure.

It operationalizes standing only when procedure can change institutional belief.

---

## Bounded limitation

A participant may fabricate evidence, harass others, repeat finally adjudicated claims without material new information, or abuse procedure.

Standing may be narrowed, but the limitation must record scope, rationale, adjudicator, less restrictive alternatives, review, reopening, and protection of others.

For consequential cases, the seriousness threshold and independent-review trigger should be established by prior rule or reviewed by a differently situated authority—not invented solely by the challenged institution.

---

## What the case now demonstrates

The case demonstrates:

- formal contestability may coexist with epistemic unsafety;
- complexity may be ingested while the complex person is discounted as a knower;
- allocated standing and realized epistemic safety are analytically distinguishable through policy and process evidence;
- declared paths require reachability testing;
- and standing-allocation disputes can be governed inside CDP Adjudicate without an infinite regress of separate tribunals.

The case does not prove that standing is the final or necessary constitutional primitive.

It does not yet defeat recognition, dignity, participation, non-exclusion, witness, care, or justice as rival grounding axioms.

That is the work of `culture/candidate-constitutional-primitives.md`.

---

## Closing test

For every materially affected participant:

> **Name one plausible contribution available in that participant's own domain that can change the controlling account, and show through policy and audit evidence that the path is reachable.**

When no such path exists, determine whether the failure is allocation, realization, contestability, or more than one.

Do not let an immaculate procedure hide an epistemically optional person.
