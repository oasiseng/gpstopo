# Construction Layout / Staking QC Plan

## Purpose & scope

Provide contractors with layout coordinates, staking reports, and reference diagrams that translate design intent to the field with construction-grade tolerances. QC emphasizes control transfer, point computation integrity, and documentation that supports inspections.

## Governing standards & references

- NSPS/ACSM Accuracy Standards for Land Surveys – construction layout section.
- ACI 117-10 (or latest) Tolerances for Concrete Construction and Materials (for structural elements).
- State Board rules for construction staking under PLS supervision.
- Project-specific design drawings, RFIs, and addenda supplied by the design professional.

## Roles & sign-offs

| Stage | Owner | QC gate |
|-------|-------|---------|
| Scope review & control selection | Project Manager + PLS | Written authorization from design professional |
| Point computation & upload | Office Engineer/Drafter | Peer review of coordinate list |
| Field layout & verification | Field Partner | Two independent check shots per setup |
| QC review | QC Lead / PLS | Signoff on stake report + diagram |
| Delivery | PM | Release package + confirmation with contractor |

## QC workflow

### 1. Pre-field intake
- Confirm latest IFC (Issued for Construction) drawings; verify revision level.
- Identify control network (project benchmarks, grid, datum) and import to project CAD.
- Define tolerance requirements per discipline (e.g., ±0.02 ft for anchor bolts, ±0.05 ft for grading stakes).
- Generate point naming convention and layer standards (e.g., `STK-###`).

### 2. Coordinate computation
- Compute layout points from design geometry; lock all inputs (offsets, rotations) in a computation log.
- Run independent check by second drafter/engineer comparing raw design vs. computed coordinates.
- Export point files (CSV/PNX) and field controller files; verify units and CRS.
- Document any assumptions (e.g., shifted grid, localized site calibration).

### 3. Field execution
- Perform site calibration or localization; record residuals (target ≤0.03 ft horizontal, ≤0.05 ft vertical).
- Stake points with two-person verification when critical (foundation corners, anchor bolts).
- Record as-built measurements: delta from design, height of point, reference offsets.
- Capture stake photos if required by client and upload daily.

### 4. QC review
- Compare recorded deltas to allowable tolerances; highlight any exceedance.
- Ensure stake report lists point ID, description, design coordinates, set coordinates, delta, date, crew.
- Review reference diagram for clarity (north arrow, control, offsets).
- Confirm revisions or RFIs incorporated; if design changed mid-project, include revision note.

### 5. Delivery & retention
- Package staking report (PDF), coordinate list (CSV), controller file, and diagram.
- Provide contractor instructions covering stake protection and validity window.
- Retain computation logs, localization files, and QC checklist for project duration + 5 years.

## Accuracy & tolerance targets

| Element | Target |
|---------|--------|
| Localization residuals | ≤0.03 ft horizontal, ≤0.05 ft vertical |
| Critical structural points | ±0.02 ft (horizontal), ±0.02 ft (vertical) unless design states otherwise |
| General layout points | ±0.05 ft horizontal |
| Reported delta rounding | 0.01 ft |

## Stage checklists

### Intake / Computation
- [ ] Latest IFC drawings logged.
- [ ] Control and datum verified by PLS.
- [ ] Point computation log reviewed by peer.
- [ ] Controller export tested.

### Field
- [ ] Localization/backsight recorded.
- [ ] Dual checks on critical stakes.
- [ ] Stake markings legible and weatherproof.
- [ ] Photos uploaded (if required).

### QC & Delivery
- [ ] Deltas summarized versus tolerances.
- [ ] Report + diagram cross-referenced.
- [ ] Contractor notified with confirmation logged.
- [ ] Records archived.

## Nonconformance handling

- **Tolerance exceeded:** Notify contractor and design team immediately; restake after resolving control or design discrepancy. Document corrective action on QC log.
- **Missing/incorrect design data:** Hold layout until RFIs resolved; escalate to PM/PLS.
- **Controller/coordinate mismatch:** Treat as major defect; regenerate files, mark superseded versions, and communicate revision.
- Track instances of rework to evaluate field partner performance and training needs.
