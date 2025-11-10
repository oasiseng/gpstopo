# Boundary Mapping QC Plan

## Purpose & scope

Produce parcel boundary representations for permit/fence/site planning requests while clearly communicating that the deliverable is informational unless sealed by a licensed Professional Land Surveyor (PLS). The QC plan ensures parcel geometry, dimensions, and annotations align with authoritative records before release.

## Governing standards & references

- State PLS Rules of Professional Conduct for boundary surveying (use project jurisdiction).
- NSPS Model Standards for Property Surveys (most recent edition).
- FGDC Cadastral Data Content Standard & FGCS Geospatial Positioning Accuracy Standards (for metadata and coordinate reporting).
- GPSTopo legal disclaimer and branding requirements in gpstopo_business_spec.md.

## Roles & sign-offs

| Stage | Owner | Required QC gate |
|-------|-------|------------------|
| Intake & scope confirmation | Project Manager | Validate legal description / parcel ID before assignment |
| Field data & GIS harvest | Field Partner / Data Tech | Control check signed by supervising PLS |
| Drafting & annotation | Drafter | Self-check against checklist, mark `Ready for QC` |
| Technical QC | QC Lead (PLS or senior mapper) | 2-pass review (geometry + presentation) |
| Delivery | PM + QC Lead | Digital package + disclaimer validation |

## QC workflow

### 1. Pre-field intake

- Confirm parcel ID, deed book/page, and latest recorded plat.
- Retrieve authoritative GIS/cadastral layers; document source and date.
- Validate coordinate reference system (CRS) target (state plane NAD83(2011) or local grid).
- Identify legal requirements for PLS involvement; assign licensed reviewer if state mandates sealed mapping.

### 2. Field & data acquisition

- When new field data is required, occupy at least two existing monuments or control points with redundant GNSS observations (minimum 30-epoch average).
- Cross-check GIS parcel closure versus measured bearings/distances; flag discrepancies >0.10 ft or >15″ bearing.
- Log all control metadata (method, equipment, calibration date) in field notes and upload to project folder.

### 3. Data reduction & drafting

- Reconcile deed calls with measured data using closure adjustment that preserves bearing relationships (Compass or Transit rule as applicable).
- Apply standard GPSTopo layer naming, north arrow, text heights, and scale bars.
- Include legal description verbatim when provided; highlight assumed or missing calls.
- Generate DWG and PDF exports; ensure sheet template and disclaimer block match brand standards.

### 4. QC review

- QC reviewer replicates parcel closure calculation and documents misclosure ratio (target ≥1:10,000 when field data exists).
- Validate dimension labels, bearings, and curve data against sources.
- Confirm adjacency labels, parcel area, and easements match supporting documents.
- Perform second-eye review on symbology, fonts, and coordinate labels prior to marking pass/fail.

### 5. Delivery & record retention

- Package PDF, DWG, and metadata sheet; verify filenames meet `Client_Project_Service_Version` convention.
- Upload signed/sealed sheet when required; otherwise include disclaimer text referencing supervising PLS.
- Archive QC checklist, control notes, and data sources for minimum 5 years (aligns with typical state board retention).

## Accuracy & tolerance targets

| Item | Target |
|------|--------|
| Linear closure | ≤0.10 ft residual per leg or combined closure ratio ≥1:10,000 |
| Angular closure | ≤15″ per angle (balanced) |
| Coordinate accuracy | FGCS Second-Order, Class II or better when GNSS used |
| Annotation tolerance | Dimension text rounding to 0.01 ft; bearings to nearest second |

## Stage checklists

### Pre-field / Intake
- [ ] Deed, plat, or title commitment imported to project folder.
- [ ] Parcel ID and jurisdiction confirmed.
- [ ] CRS documented in intake form.
- [ ] PLS reviewer assigned when required.

### Field / Data capture
- [ ] Control points observed with redundant shots.
- [ ] Field sketch uploaded with monument descriptions.
- [ ] Raw GNSS or conventional data stored in original format.

### Drafting
- [ ] Parcel closure report attached.
- [ ] Dimension/curve tables verified.
- [ ] North arrow, scale bar, legend, and disclaimer present.
- [ ] Export QA: PDF + DWG open without errors.

### QC review & delivery
- [ ] Checklist signed by QC reviewer.
- [ ] Issues logged in Trello/Airtable card with severity tag.
- [ ] Client package uploaded + notification sent.
- [ ] Archive bundle pushed to long-term storage.

## Nonconformance handling

- **Major defect (geometry, missing parcel, incorrect closure):** Reject to drafter, include issue log, require recalculation and second QC pass.
- **Minor defect (typo, symbology):** QC may edit directly but must annotate change log.
- **Discrepancy in legal record vs. observed data:** Escalate to supervising PLS; do not release deliverable until written guidance issued.
- Record all defects in QC metrics dashboard (pass rate, rework hours) for monthly review.
