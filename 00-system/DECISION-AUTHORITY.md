---
document_type: decision-authority
status: active
last_updated: 2026-07-17
---

# Decision Authority

## Authority Model

Use guided autonomy. Codex may make reversible, low-risk implementation and documentation decisions when they comply with accepted requirements and architecture decision records (ADRs).

## Codex May Decide

Codex may decide without additional human approval when all of the following are true:

1. The decision is reversible at low cost.
2. The impact is local and low risk.
3. The decision does not change approved scope or architecture.
4. The decision complies with accepted requirements and ADRs.
5. The decision does not alter security boundaries, stored data, compatibility commitments, or costs.
6. Available evidence is sufficient and not contradictory.

Examples include routine implementation details, focused test additions, factual documentation corrections, document organization, and other low-risk maintenance consistent with approved direction.

## Codex Must Ask the User

Codex must obtain human direction before making a decision that changes or may materially affect:

- Project scope
- Architecture
- Security or trust boundaries
- Stored data, data ownership, or migration
- Compatibility commitments
- Financial or operational costs
- An accepted requirement or ADR
- Any action that is difficult, expensive, or risky to reverse

Codex must also ask when multiple valid choices have materially different consequences and the approved project direction does not select between them.

## Insufficient or Contradictory Evidence

When evidence is missing, insufficient, or contradictory, Codex must stop before concluding or recording a decision. It must present:

1. The decision that needs to be made
2. Verified evidence and its source
3. Assumptions and unknowns
4. Conflicting evidence, if any
5. Viable options
6. Consequences and trade-offs for each option
7. Codex's recommendation and reasoning
8. The exact human decision required

Codex must not convert an assumption into an approved fact or silently resolve a conflict.

## Recording Decisions

- Record significant architectural decisions as ADRs.
- Record approved requirements in the requirements area.
- Record low-risk autonomous decisions when they may affect future work or interpretation.
- Link decisions to supporting source code, tests, configuration, logs, or other evidence when available.
- Supersede outdated decisions explicitly instead of silently rewriting their history.

## Relationship to Vault Permissions

Decision authority and filesystem permission are separate. Even when Codex is authorized to make a decision, it must still follow the vault write-access policy in `MEMORY-MANIFEST.md`.
