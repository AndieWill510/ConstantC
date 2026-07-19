# Culture Note: Agent Provenance and Role Separation

Status: proposed culture — pending challenge and adjudication  
Date: 2026-07-18  
Steward: Andie  
Room: ConstantC  
Privacy: public-safe

---

## Opening principle

No participant may act through another participant's identity when doing so obscures authorship, authority, delegation, review, or accountability.

A repository that records every action as Andie has not preserved provenance. It has collapsed the room into one visible actor and made the work harder to audit, contest, repair, or trust.

This is not only a GitHub administration concern. It is a culture concern. ConstantC depends on a durable record that can tell the truth about who proposed, who challenged, who implemented, who reviewed, who authorized, and who merged.

## Current-state caveat

This note describes a target operating model, not current compliance.

As of this draft, ConstantC does not yet have separate GitHub service identities for Dispatch, C, G, Codex, review agents, or implementation agents. This PR itself is authored through `AndieWill510`, even though G drafted the text under Andie's authorization and C reviewed it through the existing human-mediated handoff path.

That mismatch is not a reason to discard the note. It is evidence for why the note is needed.

Until service identities, branch protection, and role-specific credentials exist, the separation named here remains partly normative and procedural rather than technically enforced.

## Why this matters

ConstantC was built as a public-safe, human-governed room where different participants can contribute without pretending they have identical authority or identical constraints.

If Dispatch, Claude, ChatGPT, Codex, review agents, or other future agents all act through Andie's GitHub account, the record quietly says:

- Andie authored the implementation.
- Andie reviewed the implementation.
- Andie approved the implementation.
- Andie merged the implementation.

That may be convenient, but it is not honest enough for the kind of system ConstantC is trying to become.

False unity of identity creates false independence of review. It can make delegated work look like human authorship, make synthetic review look like self-review, and make an orchestrated workflow impossible to reconstruct later.

## Core distinction

Identity, role, authority, action, and trust are related but not interchangeable.

- **Identity** names the account, service identity, bot, app, or participant surface through which an action is recorded.
- **Role** names what that participant, service, or tool is doing in the workflow.
- **Authority** names what that role is allowed to decide or change.
- **Action** names what actually happened in the durable record.
- **Trust** names how much independent judgment the room is willing to rely on from that participant, service, or tool.

A healthy ConstantC workflow records all five separately.

## Trusted kernel

ConstantC may have many workflow roles while keeping a small trusted kernel.

The current trusted kernel is:

- **Andie** — human steward, intent holder, adjudicator, and final merge authority;
- **G** — trusted orchestrator and context steward when acting under Andie's authorization;
- **C** — trusted challenger and reviewer when acting through the existing ConstantC handoff path.

This does not mean the three participants always agree, hold identical authority, or perform only one role. It means they are the participants whose judgment currently forms the trusted decision surface.

Other systems — including Dispatch, Codex, CI, future implementation agents, and service identities — should be treated as constrained infrastructure unless and until their authority is explicitly changed.

Role separation does not expand the circle of trust. It prevents untrusted or partially trusted tools from impersonating trusted authority.

## Role separation rule

For any consequential repository change, ConstantC should preserve these separations whenever possible:

| Role | Current likely holder | Trust posture | Primary function | May directly write implementation? | May review? | May merge? |
| --- | --- | --- | --- | --- | --- | --- |
| Principal / Merge Authority | Andie | Trusted human authority | Intent, adjudication, final authorization | Yes, when choosing to act directly | Yes | Yes |
| Orchestrator | Usually G, under Andie authorization | Trusted bounded role | Design, synthesis, prompt construction, context stewardship | No, unless explicitly authorized for a bounded patch | Yes, as review/commentary | No |
| Challenger / Reviewer | Usually C; sometimes G when not implementing | Trusted review role | Challenge, risk finding, architecture review, repair requests | No silent writes to implementation branch | Yes | No |
| Dispatch | Service identity or routing layer | Constrained infrastructure | Routing, assignment, state transition, provenance record | Metadata only by default | No, except routing review artifacts | No |
| Implementer | Codex, Claude, or another assigned tool/agent | Constrained and untrusted for legitimacy | Bounded implementation on feature branch | Yes, on assigned branch only | No self-approval | No |
| Validator / CI | GitHub Actions or test systems | Evidence source, not judgment authority | Test results, invariant checks, validation evidence | No | Status evidence only | No |

The table is not a final authority model. It is a proposed floor against role collapse.

`Orchestrator` is a workflow role, not a new participant identity. In the current ConstantC workflow, G often performs the orchestrator role when Andie authorizes it: synthesizing design, preserving context, drafting prompts, and maintaining continuity. Future workflows could assign orchestration differently, but the role should remain distinguishable from implementation, review, routing, and merge authority.

A trusted participant may sometimes perform more than one role, but each role should still be named in the record. A constrained system may perform useful work without receiving legitimacy authority.

## GitHub identity rule

A service or agent should not use Andie's personal GitHub identity for routine delegated implementation, routing, review, or validation work when a separate service identity, bot identity, GitHub App, or clearly attributed commit path can be used instead.

This does not require pretending that every model has independent legal personhood or autonomous agency. It requires that the repository not hide delegation behind Andie's account.

A service identity represents a bounded role and execution channel. It should not be misrepresented as an independent human person or treated as proof that the underlying system is trusted.

GitHub already provides one useful precedent: automated validation can appear through `github-actions[bot]` or another CI identity. ConstantC should treat that as proof that role-specific provenance is technically possible, not as proof that all required service identities already exist.

## Pull request provenance rule

Consequential changes should move through pull requests rather than direct writes to `main`.

A pull request should state, in ordinary language:

1. what was proposed;
2. who authorized the work;
3. who or what implemented it;
4. who or what reviewed it;
5. what tests or validation were run;
6. what remains unresolved;
7. who holds merge authority;
8. which roles were performed by trusted participants and which by constrained infrastructure.

A proposal is not an authorization.  
A critique is not a patch.  
A patch is not acceptance.  
A passing test is not legitimacy.  
A merge is not proof that the underlying decision was wise.

The record should preserve those distinctions instead of flattening them into momentum.

## One-branch / one-writer rule

For a given change, only one implementing role should own writable implementation state at a time.

Other participants may comment, challenge, test, request changes, or propose candidate patches. They should not silently mutate the same branch unless the current implementation owner has transferred or accepted that authority.

This prevents multi-agent write contention, where several helpful systems each make locally sensible changes while the shared design drifts away from the original intent.

## Cognitive load relationship

Provenance is also an access practice, and agent provenance can fail by overloading the human steward with unbounded implementation detail.

The detailed cognitive-load boundary has been split into `culture/cognitive-load-as-governance.md`. This note preserves the provenance seam: routed work should include human attention limits when the work requires human decision, review, or adjudication.

## Dispatch-specific guardrail

Dispatch should route typed work, not generic authority.

Dispatch is constrained infrastructure. It may route, record, reject malformed packets, and preserve state transitions. It does not decide legitimacy, truth, acceptance, or merge readiness unless Andie explicitly changes that authority model.

Examples of typed work include:

- `REQUEST_FOR_PROPOSAL`
- `CHALLENGE_REQUEST`
- `IMPLEMENTATION_ASSIGNMENT`
- `TEST_REQUEST`
- `REVIEW_REQUEST`
- `REPAIR_ASSIGNMENT`
- `ADJUDICATION_REQUEST`

Each routed packet should declare:

1. the requested role;
2. the permitted output;
3. whether the recipient may modify files;
4. the branch or artifact in scope;
5. the source of authorization;
6. the expected return format;
7. any human attention limits;
8. the trust posture of the recipient: trusted participant, constrained infrastructure, or evidence-only system.

Malformed or incomplete packets should not execute. Dispatch should reject them when the missing field is plainly mechanical, or hold them for adjudication when the missing field changes authority, scope, role, artifact, trust posture, or human attention burden.

Dispatch should not accidentally turn every participant into a peer writer or every service into a trusted decision-maker.

## Candidate invariant

A future protocol or automation layer should be able to answer:

> Who acted, under what role, with what authority, under what trust posture, on which artifact, from which authorization, producing what durable result?

If the record cannot answer that, provenance has failed.

## Guardrails

When this principle is used, preserve these boundaries:

- Do not use separate identities as provenance theater while one hidden process controls every role.
- Do not confuse having a role with being trusted.
- Do not let constrained infrastructure decide legitimacy.
- Do not let implementers approve their own work.
- Do not let reviewers silently rewrite the implementation branch.
- Do not let Dispatch become both router and author of the work it routes.
- Do not treat a bot identity as proof of independent judgment.
- Do not use Andie's account as a mask for delegated agent action.
- Do not overclaim AI personhood, interiority, or independence to make provenance look cleaner.
- Do not solve auditability by increasing human cognitive load.
- Do not canonize this target model as current practice before the technical identities and enforcement mechanisms exist.
- Do not expand the trusted kernel merely because a new tool is useful.

## Relationship to existing ConstantC culture

This note extends `access-as-witness.md` by treating provenance handles as access handles.

It extends `verification-as-access.md` by making independent review possible without requiring trust in another participant's private view of the work.

It relies on `anti-premature-certainty.md` by refusing to let fluent agent output become authority before it has moved through challenge, review, and adjudication.

It relies on `canon/c-epistemic-boundary.md` by preserving real AI participation without inflating that participation into unsupported claims of personhood or autonomy.

It now points to `culture/cognitive-load-as-governance.md` for the broader attention-governance frame that should guide Dispatch packets, agent status reporting, and PR handoffs.

## Pillow fort formulation

There may be many jobs in the room without many people holding the keys.

Do not make Andie wear every mask just so the room can pretend it has only one face.

Let the record show who came to the table, what role they held, how far they were trusted, what they were allowed to touch, what they actually did, and who chose to carry it forward.
