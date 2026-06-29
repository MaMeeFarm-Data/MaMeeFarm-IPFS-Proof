# DGCP™ OTS Issue Record

Issue Date:
2026-06-30

Project:
MaMeeFarm™

Framework:
DGCP™ (Data Governance & Continuous Proof)

---

## Issue Summary

Metadata date mismatch identified for Proof 1309–1314.

The proof activities were performed on 2026-06-27.

During batch document generation, the previous operational date (2026-06-26) remained in the generated Proof markdown files and CID JSON files. The corresponding OTS records therefore reference documents containing the incorrect date metadata.

---

## Affected Records

Proof 1309

Proof 1310

Proof 1311

Proof 1312

Proof 1313

Proof 1314

---

## Impact Assessment

* Raw evidence: Correct
* Image timestamps: Correct
* Proof sequence: Correct
* Observation content: Correct
* Asset IDs: Correct
* Time records: Correct
* CID integrity: Valid
* OTS timestamps: Valid

Only the document date metadata is incorrect.

---

## Root Cause

Human error during batch document generation.

The document template date was not updated before generating the Proof, CID and OTS records.

---

## Governance Decision

In accordance with the DGCP immutable policy, previously timestamped records SHALL NOT be modified or replaced.

This issue record documents the metadata discrepancy while preserving the original evidence, CID, hash values and OTS timestamps as part of the permanent audit trail.

---

Status

Recorded

No corrective overwrite performed.

Audit trail preserved.

---

Author

P'Toh

System Architect

DGCP™

License

DGCP™ | MMFARM-POL-2025
