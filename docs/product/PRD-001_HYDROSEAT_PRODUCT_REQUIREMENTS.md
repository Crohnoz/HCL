# PRD-001 — HydroSeat Product Requirements Document

**Organization:** Crohnoz Labs  
**Program:** HCL — Hardware Core Lab  
**Product:** HS-001 HydroSeat  
**Version:** 0.1.0  
**Status:** Draft  
**Baseline target:** BL-01 Requirements  

## 1. Purpose

Define the controlled product requirements for HydroSeat as a future therapeutic medical device for home use. This document governs architecture, risk management, CAD, electronics, firmware, verification, validation and design transfer.

## 2. Product vision

HydroSeat shall integrate ergonomic seating, perianal pressure unloading, controlled warm-water sitz bathing, low-intensity localized hydrotherapy, removable water containment, controlled drainage, cleanability and medical-device lifecycle controls.

The primary geometry shall prioritize a large adult body envelope while supporting smaller users through validated inserts or adjustments.

## 3. Preliminary intended use

HydroSeat is a home-use medical device intended to provide controlled pressure unloading, temperature-regulated sitz bathing and low-intensity localized hydrotherapy for temporary relief of discomfort in the perianal region, under the conditions, indications and contraindications established by the manufacturer.

This wording requires clinical and regulatory review.

## 4. Intended users and environment

Primary user: adult individual at home.  
Secondary users: caregiver, service technician and healthcare professional.

Initial assumptions:

- individual use;
- indoor domestic environment;
- user or caregiver can understand instructions;
- user can transfer safely or receives assistance;
- no pediatric, institutional or shared clinical use in the first configuration.

## 5. Product architecture

```text
HS-001 HydroSeat
├── HS-100 Structural Seating System
├── HS-200 Anatomical Support Interface
├── HS-300 Removable Basin System
├── HS-400 Thermal Management System
├── HS-500 Hydrotherapy Flow System
├── HS-600 Drainage and Cleaning System
├── HS-700 Electrical and Control System
├── HS-800 User Interface and Safety Indication
└── HS-900 Accessories and Service Items
```

## 6. Design principles

1. Safety by design before warnings.
2. User weight shall never be supported by the basin.
3. Wet and electrical zones shall be physically separated.
4. Cleaning is a primary function.
5. Final materials and components shall be traceable.
6. Requirements, risks and tests shall remain linked.
7. Prototype substitutions shall not represent final conformity.
8. No commercial release without verified requirements and applicable authorization.

## 7. Core functional requirements

- `PRD-FUN-001`: unload direct pressure from the intended perianal treatment region.
- `PRD-FUN-002`: support user loads through a dedicated structural frame.
- `PRD-FUN-003`: permit controlled partial immersion in warm water.
- `PRD-FUN-004`: provide a removable basin for filling, emptying and cleaning.
- `PRD-FUN-005`: provide low-intensity localized water flow.
- `PRD-FUN-006`: maintain water temperature within a validated range.
- `PRD-FUN-007`: provide controlled drainage.
- `PRD-FUN-008`: permit immediate shutdown of active functions.
- `PRD-FUN-009`: indicate correct basin installation.
- `PRD-FUN-010`: support a hygienic drying-towel accessory.

## 8. Core safety requirements

- `PRD-SAF-001`: prevent water temperature above the validated limit in normal and single-fault conditions.
- `PRD-SAF-002`: use independent thermal protection.
- `PRD-SAF-003`: separate hazardous electrical energy from the wet zone.
- `PRD-SAF-004`: withstand declared user mass and dynamic loads.
- `PRD-SAF-005`: resist tipping during transfer and repositioning.
- `PRD-SAF-006`: limit hydrojet pressure and suction.
- `PRD-SAF-007`: control overflow, splash and displacement.
- `PRD-SAF-008`: prevent unintended basin release.
- `PRD-SAF-009`: enter a safe state after relevant faults.
- `PRD-SAF-010`: prevent automatic restart after power restoration.

## 9. Ergonomic requirements

- prioritize a high-percentile adult body envelope;
- support smaller users through validated adaptation;
- avoid unacceptable thigh compression;
- stabilize the pelvis;
- preserve safe sitting and standing transfer;
- maintain acceptable seat height;
- meet a validated comfort target for intended session duration.

## 10. Hygiene and material requirements

- wet-path components shall be removable or fully accessible;
- geometry shall minimize retained water and inaccessible crevices;
- cleaning and drying shall be validated;
- final materials shall be identified by manufacturer, grade and approved supplier;
- biological evaluation shall be based on contact type, duration, temperature and cleaning chemistry;
- no material shall be accepted solely because it is marketed as “medical grade”;
- 3D-printed wet-path or patient-contact parts require specific process validation.

## 11. Electrical and control requirements

- prefer an approved external power supply and low voltage at the chair;
- include overcurrent protection;
- detect relevant sensor faults where feasible;
- prevent heating without validated water and sensor conditions;
- use keyed, protected connectors;
- configuration-control firmware;
- assess every safety-relevant software change for regression impact.

## 12. Preliminary engineering targets

| Parameter | Initial target |
|---|---:|
| Declared user mass | At least 150 kg |
| Nominal water temperature | 37–38 °C |
| Upper temperature limit | Not greater than 40 °C, pending clinical validation |
| Working basin volume | Approximately 2–5 L |
| Basin removal time | Less than 2 minutes |
| Routine cleaning time | Less than 10 minutes |
| Use model | Individual adult, home environment |

These values are not final medical specifications.

## 13. Quality and regulatory requirements

- develop under a QMS compatible with ISO 13485;
- maintain lifecycle risk management;
- control design inputs, outputs, reviews, verification, validation and changes;
- maintain a standards applicability matrix;
- prevent claims beyond approved intended use and evidence;
- confirm the Chilean classification and regulatory route before design freeze;
- trace each prototype and commercial unit to configuration and evidence.

## 14. Verification and validation

Every requirement shall have an objective verification method: inspection, analysis, bench test, laboratory test, software test, usability test or document review.

Validation shall use representative users and production-equivalent units to confirm intended use, comfort, transfer, filling, drainage, cleaning, controls, warnings and overall benefit-risk acceptability.

## 15. Open decisions

- Chilean risk class and submission route;
- final indications and contraindications;
- session duration and frequency;
- commercial seat architecture: integrated or universal;
- hydrojet inclusion in first release;
- final contact classification;
- cleaning agents and process;
- software safety classification;
- IP rating;
- life expectancy;
- manufacturing process.

## 16. Exit criteria for BL-01 Requirements

- intended use reviewed;
- user needs approved;
- preliminary classification documented;
- preliminary hazard analysis opened;
- requirements uniquely identified;
- verification methods assigned;
- open assumptions assigned to owners;
- formal design review completed.
