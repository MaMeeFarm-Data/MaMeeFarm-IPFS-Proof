# DGCP™ Proof System — MaMeeFarm™  
Version: README V2 (2025-12)  
License: MMFARM-POL-2025  

DGCP™ (Data Governance & Continuous Proof) is the unified protocol for capturing,  
structuring, validating, and timestamping Real-World Data (RWD) at MaMeeFarm™.

Every Proof in this repository represents a verifiable real-world event  
anchored via **IPFS + SHA-256 + OpenTimeStamp (OTS)** and governed under  
the **append-only** rule.

---

# 1. Core Principles (V2)

All Proofs must be:

- **Real** — captured from actual human labor or environmental conditions  
- **Traceable** — CID → Proof MD/JSON → SHA256 → OTS  
- **Append-only** — files never overwritten; corrections must use new files  
- **Timestamped** — both local time (+07) and external cryptographic time  
- **Human + machine readable** — MD for humans, JSON for machines  

---

# 2. Repository Structure (V2)

/proof/
proof_XXX.md
proof_XXX.json

/daily/2025/
YYYY-MM-DD-daily-log.md

/daily/json2025/
YYYY-MM-DD-daily-log.json

/ots/
proof_XXX.sha256
proof_XXX.ots

/ipfs-index/
proof_XXX_ipfs.txt


---

# 3. DGCP Proof Standard (V2)

Each Proof = **two files**:

proof_XXX.md
proof_XXX.json

Both must reference the same CID and represent one real event.

---

## 3.1 Proof Markdown (MD) Format

A valid Proof MD includes the following sections in order:

1. **Title** — `DGCP™ Continuous Proof — Proof_XXX`  
2. **Timestamp** — local time + date  
3. **Event Summary** — concise description  
4. **Evidence Metadata**  
   - Filename  
   - IPFS CID  
   - IPFS URL  
5. **Observations**  
   - DGCP Unit classification  
   - Context-specific values (temperature, egg weight, crop stage, etc.)  
6. **Notes** — relevance to DGCP  
7. **Correction Log (optional)**  
8. **License footer:**  
MMFARM-POL-2025

---

## 3.2 Proof JSON Format (Unified Schema)

```json
{
"proof_id": "Proof_XXX",
"date": "YYYY-MM-DD",
"time_local": "HH:MM",
"location": "MaMeeFarm, Lampang, Thailand",
"media": {
 "file": "filename.jpg",
 "cid": "bafy...",
 "ipfs_link": "https://..."
},
"category": "DGCP Unit",
"observations": {},
"sha256": "",
"ots_receipt": "",
"license": "MMFARM-POL-2025"
}
```
This schema is locked for V2.

## 4. IPFS Workflow (Pinata Standard)

Each Proof must:

Pin at least one media file to IPFS

Save CID inside MD and JSON

Save a CID-only record inside:
/ipfs-index/proof_XXX_ipfs.txt
Filenames must be < 50 chars for global compatibility.
## 5. SHA-256 + OpenTimeStamp (OTS) Workflow

After finalizing MD + JSON:

Export both files

Compute SHA-256 hash

Submit hash → OTS

Save outputs:
ots/proof_XXX.sha256
ots/proof_XXX.ots
Add SHA-256 + OTS filename to the JSON file

Never modify the original proof content afterward

OTS = cryptographic proof that the event existed on that date.
## 6. Daily Log Standard (V2)

Two daily logs must be created:

6.1 Markdown Daily Log
daily/2025/YYYY-MM-DD-daily-log.md
Must include:

Summary

All Proof events (IDs, times, units, CIDs)

Correction logs (if any)

CID index

License footer

6.2 JSON Daily Log
daily/json2025/YYYY-MM-DD-daily-log.json
Machine-readable list of all proofs that day.
## 7. DGCP Unit Taxonomy (V2)

Each Proof must belong to one and only one DGCP Unit:

Egg Output Unit

Environmental Monitoring Unit

Livestock-Care Action Unit

Animal Welfare Monitoring Unit

Human-Care Behavior Unit

Human-Support Nutrition Unit

Crop-Growth Observation Unit

Crop-Readiness Biological Unit

RWD Crop Harvest Unit

Daily Environmental Stability Unit

Survival & Labor Unit

Ground-Truth Real-Life Unit

Unit names must not be changed.

## 8. Append-Only Policy

DGCP prohibits deletion or modification of original Proof files.

When an error is found:

Keep the original file

Add corrected file:
proof_XXX_corrected.md
Log correction in that day's Daily Log

Commit as a new append-only change

Transparency = required for long-term trust.
## 9. License Requirement

Every file must end with the following:
MMFARM-POL-2025 — Proof-of-Life & Real-World Data License
Unauthorized training, reproduction, or derivative modeling prohibited.
End of README V2 (2025 Unified Standard)
