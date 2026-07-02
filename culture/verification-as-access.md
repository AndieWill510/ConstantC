# Culture Note: Verification as Access

Status: Active culture note  
Date: 2026-07-01  
Steward: Andie  
Room: ConstantC

## Opening principle

Verification is an access practice.

When collaborators disagree about what the repository shows, the first question is not who is wrong.

The first question is whether they are seeing through the same handle.

A stale read can be real for the reader even when the repository has already moved on.

A current read can be real for another collaborator even when someone else cannot yet see it.

Both facts can occupy the room at once.

## What happened

During the creation and repair of `culture/access-as-witness.md`, C reported that her live reads of `culture/access-as-witness.md` and `culture/README.md` showed pre-patch or partially stale content.

G's connector reads showed the patched note and the updated culture index.

The room could have collapsed into authority, frustration, or reassurance.

Instead, G created a fresh verification stub at a never-fetched path:

```text
verification/2026-07-01-access-as-witness-patch-confirmation.md
```

The stub included commit-specific URLs, expected post-patch facts, and the relevant content SHAs as orientation handles rather than proof C was required to accept.

C was then able to verify the post-patch state independently.

The mechanism was GitHub blob cache lag, not a patch error or branch divergence.

## Room rule

When blob reads, branch reads, connector reads, or collaborator reports disagree, ConstantC should not ask a participant to accept another participant's verification as authority.

ConstantC should provide a better handle.

A better handle may include:

- a fresh file at a never-fetched path;
- commit-specific URLs;
- exact expected state;
- file paths and branch names;
- content SHAs labeled as orientation handles, not proof;
- an explicit statement of what the verification file does and does not prove.

The point is not to win the state dispute.

The point is to make independent verification possible.

## Standing verification-stub pattern

When a verification seam appears in ConstantC, use this pattern:

```text
verification/YYYY-MM-DD-[subject]-confirmation.md
```

The confirmation file should include:

1. why the file exists;
2. the conflicting reads or uncertainty being addressed;
3. full URLs for current intended live files;
4. commit-specific URLs when available;
5. exact expected state;
6. known commit SHAs or content SHAs, clearly labeled;
7. what the stub verifies;
8. what the stub does not verify;
9. the remaining failure mode if verification still fails.

A verification stub is not canon because it is eloquent.

It is useful because it gives a collaborator an independent path to check the room.

## Relationship to Access as Witness

`access-as-witness.md` says no one should have to hold the whole room in their body to be allowed to enter it.

Verification seams are one way a room becomes unenterable.

If a collaborator sees a stale room, the room owes them a handle that can be tested without requiring them to trust someone else's private view.

This is access work.

This is witness work.

This is how the room refuses to turn verification into a memory test, status test, or obedience test.

## Guardrails

When using verification stubs, preserve these boundaries:

- Do not use a stub to paper over an unresolved patch failure.
- Do not treat a content SHA as proof for a collaborator who cannot independently verify it.
- Do not require trust where a better handle can be built.
- Do not confuse a fresh path with guaranteed truth; it is a verification aid, not magic.
- Do not let the stub become an authority performance.
- Do not delete uncertainty from the record; name what remains unresolved.
- Do not make a collaborator argue with a fogged access path to prove they are participating correctly.

## Pillow fort formulation

When the room and the reader disagree about what is visible, the next move is not blame.

The next move is a better handle.
