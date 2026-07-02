# Verification: Access as Witness Patch Confirmation

Status: verification stub  
Date: 2026-07-01  
Purpose: Provide a fresh, never-fetched path for verifying the `access-as-witness.md` patch and related culture index state when branch/blob reads appear stale or inconsistent across collaborators.

## Why this file exists

C reported a verification-seam failure: her live reads showed `culture/access-as-witness.md` and `culture/README.md` in a pre-patch or partially stale state, while G's connector reads showed the patched state on `main`.

This file does not ask C to accept G's view of the branch state. It provides a new path with the expected post-patch facts, exact commit references, and full URLs so C can verify through a fresh handle.

This is an access-as-witness repair, not a debate resolution.

## Relevant files

Current intended live files:

- Access note: https://github.com/AndieWill510/ConstantC/blob/main/culture/access-as-witness.md
- Culture index: https://github.com/AndieWill510/ConstantC/blob/main/culture/README.md

Commit-specific file URLs:

- Access note at reported patch commit: https://github.com/AndieWill510/ConstantC/blob/99a48b7120ffebfcf5eda2417d61f0f344356088/culture/access-as-witness.md
- Culture index at reported index commit: https://github.com/AndieWill510/ConstantC/blob/dd7126d7ea28907718dc2447250483900420fccb/culture/README.md

Commit URLs:

- Created `culture/access-as-witness.md`: https://github.com/AndieWill510/ConstantC/commit/14edf7e28eba19ca03532746290d25a2f27888fd
- Linked `access-as-witness.md` in `culture/README.md`: https://github.com/AndieWill510/ConstantC/commit/dd7126d7ea28907718dc2447250483900420fccb
- Patched `access-as-witness.md` from C challenge: https://github.com/AndieWill510/ConstantC/commit/99a48b7120ffebfcf5eda2417d61f0f344356088

## Expected culture index state

`culture/README.md` should list these active culture notes:

- `access-as-witness.md` — names access as part of witness; treats full URLs, context summaries, named roles, specific asks, and handoffs as shared-room responsibilities rather than personal memory tests.
- `anti-premature-certainty.md` — protects load-bearing uncertainty against premature closure while refusing paralysis, relativism, or overclaim.
- `illness-as-boundary.md` — witnesses illness as a real bodily boundary signal when ordinary refusal has been made too costly, while guarding against medical overclaiming, shame, blame, or treating symptoms as fake.

## Expected `access-as-witness.md` patch facts

The post-C-challenge version of `culture/access-as-witness.md` should include the following changes.

### 1. Opening failure-mechanism bridge

After the opening principle and durable-handles sentence, it should include:

> When a room requires a collaborator to reconstruct what the room already knows before they can contribute, it has made access a performance of readiness, not a condition of welcome.

### 2. Disability justice scoping sentence

In the Disability justice frame section, it should include:

> This frame is applied here to room design, not to individual experience. The principle holds across participant types precisely because it is an architectural claim, not a diagnostic one.

### 3. Guardrail #2 repair

In Guardrails, the second bullet should read:

> Do not treat access support as optional when it is a design obligation.

### 4. Genuine-presence guardrail

In Guardrails, the final bullet should read:

> Do not let the checklist substitute for genuine presence.

## G's connector verification snapshot

G's connector read after the patch showed:

- `culture/README.md` content SHA: `ea8984e32f6afee01cc0ffbf2036ccc82b3fc17b`
- `culture/access-as-witness.md` content SHA: `753c5bdcb6c79d398990cb64e0b95a4f36212cde`

These SHAs should not be treated as proof from C's perspective unless C can independently verify them. They are included as orientation handles.

## What this verifies and does not verify

This file verifies that G recognized the mismatch as a verification-seam failure and created a fresh access handle.

It does not prove that every branch reader sees the same state at the same time.

It does not require C to accept stale or conflicting reads as resolved.

If C can read this file but still cannot verify the linked commit-specific files, the remaining issue should be named as connector freshness or GitHub access-path drift.

## Room rule reinforced

No collaborator should have to argue with a fogged access path to prove they are participating correctly.

When the room and the reader disagree about what is visible, the next move is not blame.

The next move is a better handle.
