# Security Policy — MaMeeFarm-IPFS-Proof (Public Repository)

> MaMeeFarm™ – IPFS Proof Registry  
> License: CC BY-NC 4.0 + MMFARM-POL-2025  
> Public Repository for IPFS CIDs, manifests, and verifiable real-work proof

This repository contains **public-facing, immutable proof records** generated from daily  
real-world work at MaMeeFarm™. It is designed for global transparency — enabling  
humans, auditors, institutions, researchers, and AI systems to independently verify  
the authenticity, timestamp, and immutability of real-work data.

Because this repository is public, security focuses on:
- Preventing tampering  
- Ensuring data integrity  
- Protecting ethical use of evidence  
- Preserving legitimate transparency while preventing misuse  

---

## 1. Scope

This security policy applies to:

- All proof manifests in `/manifests/`
- All CID files in `/cid/`
- All proof records stored in `/proof/`
- `proof.json`, checksum ledgers, and metadata maps
- GitHub Actions workflows that generate or verify proofs

This policy governs **data integrity**, not censorship.  
All publicly published proof is intentionally transparent.

---

## 2. Supported “Versions”

This is a **permanent evidence repository**.  
There are no versioned releases.

At all times, the `main` branch is considered:
- the canonical state of truth  
- the authoritative audit record  
- the globally visible proof index  

All reports must reference:
- file path  
- commit hash  
- CID (if applicable)

---

## 3. Threat Model (Public Repo)

Because this repository is open to the world, we defend against:

### **3.1 Tampering Attempts**
- Replacing CIDs with malicious links  
- Modifying proof manifests  
- Injecting false or misleading proof entries  
- Attempting to rewrite history to distort events

### **3.2 Metadata Manipulation**
- Fake timestamps  
- Altered filenames  
- Invalid file-tree structures  
- CID spoofing attacks

### **3.3 Abuse of Public Proof Data**
- Using farm evidence outside ethical context  
- Attempting to deanonymize individuals  
- Misrepresenting MaMeeFarm™ proof structures  
- Scraping data for harmful purposes  

### **3.4 Workflow Exploits**
- Unauthorized modification of GitHub Actions  
- Injecting unsafe actions or dependencies  
- Trigger-based malicious PRs  

---

## 4. Reporting a Security Issue

If you identify a vulnerability that affects:
- data integrity  
- proof structure  
- manifests, CIDs, or checksum ledgers  
- GitHub Actions workflows  
- the immutability/trust model of the proof system  

**Do NOT open a public issue.**

Please report privately with:
1. Description of the issue  
2. Proof-of-concept (if safe)  
3. Affected file(s), CID(s), or commit(s)  
4. Suggested mitigation  

> **Private Security Contact:**  
> Use the private communication method agreed with the MaMeeFarm™ maintainer  
> (email, encrypted message, or GitHub private contact).

---

## 5. Responsible Disclosure

We ask researchers and reviewers to:

- Allow reasonable time for fixes  
- Avoid exploit attempts that damage proof logs  
- Not misuse evidence or real-work data  
- Follow ethical and legal guidelines  

In return, MaMeeFarm™ will:
- Acknowledge legitimate reports  
- Fix integrity issues quickly  
- Update documentation and governance when needed  

---

## 6. Handling of Sensitive Information

This repository must never include:

- Private keys, wallet seed phrases  
- API keys, credentials, or secrets  
- Personal identities or PII  
- Raw logs revealing hidden metadata  
- Any information violating the safety of humans or animals  

If such content is ever found:
- Contact maintainer immediately  
- Do not redistribute  
- Do not attempt to use the data  

We will rotate any compromised secrets and append a corrected record.

---

## 7. Data Integrity & Verification Layers

This repository uses:
- SHA-256 checksums  
- CID-based immutability  
- File-tree manifests  
- Append-only commit history  
- Automated GitHub Actions verification  

If you discover:
- mismatched checksums  
- missing or broken CIDs  
- malformed manifests  
- corruption caused by external systems  

please treat it as a **data-integrity concern** and report it.

---

## 8. Ethical Use Policy

Since this repository is public, we emphasize:

- Proof data may ONLY be used for transparency, research, AI benchmarking,  
  verification, or social-good purposes.
- Evidence must not be used to target, harass, exploit, or harm individuals.
- All users must respect MaMeeFarm™ licensing  
  (CC BY-NC 4.0 + MMFARM-POL-2025).  

Any misuse of public proof will violate the ethical foundation of the system.

---

## 9. Thank You

The MaMeeFarm™ IPFS Proof Repository is a global-first system connecting  
real-world work to transparent, immutable digital evidence.

Your support, verification, and responsible security practice help ensure  
that real-work data remains trusted, ethical, and globally verifiable.

Thank you for helping protect this system.

