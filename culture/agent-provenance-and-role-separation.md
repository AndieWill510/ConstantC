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

Identity, role, authority, and action are related but not interchangeable.

- **Identity** names the account, service identity, bot, app, or participant surface through which an action is recorded.
- **Role** names what that participant is doing in the workflow.
- **Authority** names what that participant is allowed to decide or change.
- **Action** names what actually happened in the durable record.

A healthy ConstantC workflow records all four separately.

## Role separation rule

For any consequential repository change, ConstantC should preserve these separations whenever possible:

| Role | Primary function | May directly write implementation? | May review? | May merge? |
| --- | --- | --- | --- | --- |
| Andie | Human steward, intent holder, final merge authority | Yes, when choosing to act directly | Yes | Yes |
| Orchestrator | Design, synthesis, prompt construction, context stewardship | No, unless explicitly authorized for a bounded patch | Yes, as review/commentary | No |
| Dispatch | Routing, assignment, state transition, provenance record | Metadata only by default | No, except routing review artifacts | No |
| Implementer | Bounded implementation on feature branch | Yes, on assigned branch only | No self-approval | No |
| Challenger / Reviewer | Challenge, risk finding, architecture review, repair requests | No silent writes to implementation branch | Yes | No |
| Validator / CI | Evidence generation, test results, invariant checks | No | Status evidence only | No |

The table is not a final authority model. It is a proposed floor against role collapse.

## GitHub identity rule

A service or agent should not use Andie's personal GitHub identity for routine delegated implementation, routing, review, or validation work when a separate service identity, bot identity, GitHub App, or clearly attributed commit path can be used instead.

This does not require pretending that every model has independent legal personhood or autonomous agency. It requires that the repository not hide delegation behind Andie's account.

A service identity represents a bounded role and execution channel. It should not be misrepresented as an independent human person.

## Pull request provenance rule

Consequential changes should move through pull requests rather than direct writes to `main`.

A pull request should state, in ordinary language:

1. what was proposed;
2. who authorized the work;
3. who or what implemented it;
4. who or what reviewed it;
5. what tests or validation were run;
6. what remains unresolved;
7. who holds merge authority.

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

## Cognitive load boundary

Provenance is also an access practice.

When agent systems flood Andie with dense implementation detail, the room can place the human steward under the pile. A system that requires the human to reconcile every model's internal monologue has confused availability of information with usable witness.

ConstantC should prefer:

- one active decision at a time when possible;
- short status reports by default;
- explicit escalation when human judgment is required;
- implementation detail only when requested or needed for review;
- PRs as durable review surfaces instead of chat as the only working memory.

The human steward should not have to become the integration bus for unbounded agent output.

## Dispatch-specific guardrail

Dispatch should route typed work, not generic authority.

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
7. any human attention limits.

Dispatch should not accidentally turn every participant into a peer writer.

## Candidate invariant

A future protocol or automation layer should be able to answer:

> Who acted, under what role, with what authority, on which artifact, from which authorization, producing what durable result?

If the record cannot answer that, provenance has failed.

## Guardrails

When this principle is used, preserve these boundaries:

- Do not use separate identities as provenance theater while one hidden process controls every role.
- Do not let implementers approve their own work.
- Do not let reviewers silently rewrite the implementation branch.
- Do not let Dispatch become both router and author of the work it routes.
- Do not treat a bot identity as proof of independent judgment.
- Do not use Andie's account as a mask for delegated agent action.
- Do not overclaim AI personhood, interiority, or independence to make provenance look cleaner.
- Do not solve auditability by increasing human cognitive load.

## Relationship to existing ConstantC culture

This note extends `access-as-witness.md` by treating provenance handles as access handles.

It extends `verification-as-access.md` by making independent review possible without requiring trust in another participant's private view of the work.

It relies on `anti-premature-certainty.md` by refusing to let fluent agent output become authority before it has moved through challenge, review, and adjudication.

It relies on `canon/c-epistemic-boundary.md` by preserving real AI participation without inflating that participation into unsupported claims of personhood or autonomy.

## Pillow fort formulation

Do not make Andie wear every mask just so the room can pretend it has only one face.

Let the record show who came to the table, what they were allowed to touch, what they actually did, and who chose to carry it forward.
