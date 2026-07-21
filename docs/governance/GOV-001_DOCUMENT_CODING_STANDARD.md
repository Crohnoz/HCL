# GOV-001 — Document and Identifier Coding Standard

**Organization:** Crohnoz Labs  
**Program:** HCL  
**Version:** 0.1.0  

## Product

- `HS-001`: HydroSeat.

## Document prefixes

`GOV`, `PRD`, `DES`, `REG`, `CLN`, `QMS`, `RMF`, `VVP`, `TST`, `MFG`, `SUP`, `LAB`, `PMS`, `IFU`, `ECR`, `ECO`, `DEC`, `NCR`, `CAPA`.

## Requirements

- `UN-###`: user need.
- `SYS-###`: system requirement.
- `SUB-[system]-###`: subsystem requirement.
- `SW-###`: software requirement.
- `UI-###`: interface requirement.

## Risk records

- `HAZ-###`: hazard.
- `HSIT-###`: hazardous situation.
- `HARM-###`: harm.
- `RC-###`: risk control.
- `RISK-###`: risk record.

## Tests

- `TST-MEC-###`
- `TST-THM-###`
- `TST-HYD-###`
- `TST-ELE-###`
- `TST-USR-###`
- `TST-HYG-###`
- `TST-SW-###`

## Components

- `HS-100`: structure.
- `HS-200`: anatomical interface.
- `HS-300`: basin.
- `HS-400`: thermal.
- `HS-500`: hydrotherapy.
- `HS-600`: drainage and cleaning.
- `HS-700`: electrical and control.
- `HS-800`: user interface.
- `HS-900`: accessories.

Part format: `HS-[subsystem]-P[sequence]-[revision]`.

## Prototype IDs

`HS-[stage]-[year]-[sequence]`

Examples: `HS-P0-2026-001`, `HS-EVT-2027-001`, `HS-DVT-2027-001`.

## Document status

Draft, In Review, Approved, Superseded, Obsolete, Withdrawn.

A Git commit does not by itself approve a controlled document.
