# DGCP Governance Issue Log
## Case: Proof Filename Case Sensitivity & Ordering Anomaly

Date (Local): 2026-02-01  
Timezone: Asia/Bangkok  
Project: MaMeeFarm™  
Framework: DGCP  
Issue ID: ISSUE-2026-02-01-CASE-ORDER

---

## Summary
Two Proof files were committed using an uppercase prefix (`Proof_575.md`, `Proof_576.md`)
while the surrounding files use lowercase (`proof_574.md`, `proof_577.md`, `proof_578.md`).

As a result, GitHub’s lexicographic sorting places these two files
out of numerical sequence, despite correct hashes and OpenTimestamps.

---

## Affected Scope
- File naming (MD layer only)
- Repository visual ordering

Not affected:
- SHA-256 integrity
- OpenTimestamps (OTS)
- CID references
- JSON proofs

---

## Observed Behavior
GitHub sorts file names case-sensitively:
- `Proof_575.md`
- `Proof_576.md`

are displayed above:
- `proof_574.md`
- `proof_577.md`
- `proof_578.md`

This creates a visual sequence break
without altering cryptographic validity.

---

## Root Cause
Case inconsistency in file prefix (`Proof_` vs `proof_`) combined with
lexicographic sorting rules in GitHub UI.

---

## Governance Decision
No renaming, no moving, no rewriting.

Reason:
- File renaming would invalidate existing SHA-256 and OTS bindings.
- Historical integrity must be preserved.
- Visual disorder is treated as a documented system state, not an error.

---

## Resolution
Add this issue record as an interpretive layer.
No changes to the Proof files themselves.

---

## Ontology Note
Interpretation is optional.  
Existence is not.

---

## License
DGCP | MMFARM-POL-2025

