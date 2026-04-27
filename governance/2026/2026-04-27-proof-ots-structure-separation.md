# DGCP™ Governance Record — Proof / OTS Structure Separation

Date (Local): 2026-04-27  
Timezone: Asia/Bangkok  
Location: MaMeeFarm (Primary DGCP Site)  
Framework: DGCP™  
Mode: Observation • Append-only • No interpretation  

---

## Context

The DGCP Proof system expanded beyond initial single-directory handling.

Two distinct data layers are actively maintained:

1) Raw Proof Files (MD + CID)  
2) OTS Processed Files (MD + JSON)

---

## Structure Definition

### Layer 1 — Raw Proof

/ proof/1000-1999/

Contains:

- Proof MD files  
- CID JSON files  

These files represent the original, unprocessed Proof records.

---

### Layer 2 — OTS Proof

/ OTS/1000-1999/proof/

Contains:

- Proof MD files (for OTS reference)  
- OTS JSON files  

These files represent timestamp-anchored verification records.

---

## Separation Principle

- Raw Proof = Source of Truth  
- OTS Proof = Verification Layer  

No merging between layers  
No overwrite between layers  

Each layer operates independently but references the same Proof sequence.

---

## Integrity Statement

- Proof numbering remains continuous  
- No modification to existing files  
- No retroactive restructuring  
- No mixing of raw and OTS files  

All operations remain append-only.

---

## Reason

This separation ensures:

- Clear distinction between data origin and verification  
- Stable OTS workflow processing  
- Reduced operational conflict between file types  
- Scalable structure for future batch expansion  

---

## DGCP Principle Alignment

- Layer Separation Improves Traceability  
- Sequence Protects Integrity  
- Append-only System  
- Verification Layer Must Not Alter Source  

---

## Status

Active  
Applied starting from Proof1000 onward  

---

DGCP | MMFARM-POL-2025
