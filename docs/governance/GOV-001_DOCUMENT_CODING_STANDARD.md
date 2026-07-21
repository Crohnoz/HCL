# GOV-001 — Document and Identifier Coding Standard

**Organization:** Crohnoz Labs  
**Program:** HCL — Hardware Core Lab  
**Version:** 0.2.0  
**Status:** Draft  
**Canonical governance document:** Yes  

## 1. Purpose

This document is the canonical source for:

- controlled-document language;
- document identifiers;
- requirement identifiers;
- risk identifiers;
- test identifiers;
- component and prototype identifiers;
- branch and pull-request governance;
- cross-references to supporting repository documents.

Where another repository document conflicts with this standard, this document governs until a controlled revision is approved.

---

## 2. Controlled-document language policy

### 2.1 Primary language

The primary language for controlled engineering, regulatory, quality, risk, verification, validation and manufacturing records shall be **English**.

This includes:

- PRDs;
- design inputs and outputs;
- risk-management records;
- test protocols and reports;
- regulatory strategy;
- quality procedures;
- controlled CAD notes;
- manufacturing specifications;
- labeling source content;
- change requests and decisions.

### 2.2 Supporting language

Spanish may be used for:

- working notes;
- internal discussion;
- user interviews conducted in Spanish;
- Chilean regulatory quotations;
- Spanish-language labeling and instructions;
- translated summaries.

### 2.3 Translation strategy

When both languages are required:

1. the English controlled version is the source document unless explicitly designated otherwise;
2. Spanish versions shall be marked as translations;
3. both versions shall carry the same document identifier and revision;
4. translation review shall be documented;
5. discrepancies shall be resolved against the approved source version;
6. legally required Spanish labeling and instructions shall be independently reviewed.

### 2.4 Existing mixed-language records

Existing records may remain mixed during the repository-foundation phase, but every new controlled record created after approval of this revision shall follow this policy.

---

## 3. Product identifier

- `HS-001`: HydroSeat first product model.

---

## 4. Document prefixes

| Prefix | Category |
|---|---|
| GOV | Governance |
| PRD | Product requirements |
| DES | Design |
| REG | Regulatory |
| CLN | Clinical |
| QMS | Quality management |
| RMF | Risk management |
| VVP | Verification and validation planning |
| TST | Test protocol or report |
| MFG | Manufacturing |
| SUP | Supplier |
| LAB | Labeling |
| PMS | Post-market |
| IFU | Instructions for use |
| ECR | Engineering change request |
| ECO | Engineering change order |
| DEC | Decision record |
| NCR | Nonconformity |
| CAPA | Corrective and preventive action |

---

## 5. Requirement identifiers

- `UN-###`: user need.
- `SYS-###`: system requirement.
- `SUB-[subsystem]-###`: subsystem requirement.
- `SW-###`: software requirement.
- `UI-###`: user-interface requirement.

---

## 6. Risk identifiers

- `HAZ-###`: hazard.
- `HSIT-###`: hazardous situation.
- `HARM-###`: harm.
- `RC-###`: risk control.
- `RISK-###`: risk record.

---

## 7. Test identifiers

- `TST-MEC-###`
- `TST-THM-###`
- `TST-HYD-###`
- `TST-ELE-###`
- `TST-USR-###`
- `TST-HYG-###`
- `TST-SW-###`

---

## 8. Component identifiers

- `HS-100`: structural seating system.
- `HS-200`: anatomical support interface.
- `HS-300`: basin system.
- `HS-400`: thermal system.
- `HS-500`: hydrotherapy system.
- `HS-600`: drainage and cleaning system.
- `HS-700`: electrical and control system.
- `HS-800`: user interface.
- `HS-900`: accessories.

Part format:

`HS-[subsystem]-P[sequence]-[revision]`

Example:

`HS-300-P004-A`

---

## 9. Prototype identifiers

Format:

`HS-[stage]-[year]-[sequence]`

Examples:

- `HS-P0-2026-001`
- `HS-P1-2026-001`
- `HS-EVT-2027-001`
- `HS-DVT-2027-001`

---

## 10. Controlled-document status

- Draft
- In Review
- Approved
- Superseded
- Obsolete
- Withdrawn

A Git commit or merge does not by itself approve a controlled document.

---

## 11. Branch governance

### 11.1 Canonical branch flow

```text
feature/* or fix/*
        ↓
develop
        ↓
main
```

- `main`: approved baselines and controlled releases.
- `develop`: integration branch.
- `feature/*`: new work.
- `fix/*`: corrective work.
- `docs/*`: documentation-only work.
- `regulatory/*`: regulatory work.
- `risk/*`: risk-management work.

Direct commits to `main` are prohibited except for emergency repository recovery approved by the project owner.

### 11.2 Pull-request target

Feature branches shall normally target `develop`.

Pull requests from `develop` to `main` shall be used only for approved baselines or releases.

---

## 12. Pull-request requirements

Each pull request shall identify:

- objective;
- changed controlled documents;
- affected requirements;
- affected risks;
- verification or review performed;
- regulatory impact;
- required approvers;
- changelog impact;
- baseline impact.

The repository pull-request template implements these requirements.

---

## 13. Canonical governance references

This document defines the policy. Supporting documents implement it:

| Document | Purpose |
|---|---|
| `CONTRIBUTING.md` | Contributor-facing workflow summary |
| `.github/pull_request_template.md` | Required PR evidence checklist |
| `.github/ISSUE_TEMPLATE/` | Structured work intake |
| `IMPLEMENTATION.md` | Temporary package-application instructions |
| `ROADMAP_MASTER.md` | Program roadmap and gates |
| `STATUS.md` | Current project state |

Supporting documents shall link back to this standard and shall not redefine policy independently.

---

## 14. Change control

Changes to this standard require:

- an ECR or documented governance decision;
- impact review;
- update of supporting documents;
- changelog entry;
- approval before baseline use.
