# Topographic Survey QC Plan

## Purpose & scope

Deliver terrain, contour, and elevation data that meets design-grade accuracy for architects, engineers, and permitting authorities. QC focuses on positional accuracy, completeness of surface features, and metadata transparency for coordinate systems and datums.

## Governing standards & references

- ASPRS Positional Accuracy Standards for Digital Geospatial Data (2023) – Class 0.5/1 mapping guidance.
- USACE EM 1110-1-1005 (Control & Topographic Surveying) for control hierarchy.
- FGCS Standards for Geodetic Control Networks.
- FEMA Flood Insurance Rate Map (FIRM) and Elevation Certificate instructions when flood data is requested.
- GPSTopo QC workflow (process_qc_review.md) and data retention policy.

## Roles & sign-offs

| Stage | Owner | QC gate |
|-------|-------|---------|
| Scope & control plan | Project Manager + PLS | PLS approves control + datums |
| Field data collection | Field Partner | Daily control check + raw log upload |
| Point cloud / surface processing | Drafter | Automated QA (voids, density) |
| Technical QC | QC Lead (PLS/PE) | Accuracy stats + checklist |
| Delivery | PM + QC Lead | File packaging + metadata |

## QC workflow

### 1. Pre-field intake
- Define vertical datum (NAVD88) and horizontal datum (NAD83(2011) State Plane unless client specifies otherwise).
- Approve control scheme: minimum two benchmarks tied to published marks or OPUS solution.
- Document required contour interval (typically 2 ft) and supplemental deliverables (CSV, DWG, TIN).
- Confirm required feature codings (breaklines, utilities, spot grades).

### 2. Field execution
- Level loops or GNSS observations must close within 0.05√K ft (K in miles) to satisfy second-order vertical standards.
- Collect redundant shots on hardscapes, corners, and abrupt grade changes; breaklines should have ≤25 ft spacing on paved areas and ≤50 ft on natural ground.
- Drone missions: maintain 70/60 forward/side overlap, capture calibration targets, and log base station coordinates.
- Log weather, equipment serial numbers, and any obstructions impacting accuracy.

### 3. Data reduction & drafting
- Process GNSS through OPUS/RTK with baseline checks; document residuals.
- Generate point cloud or merged survey dataset; remove outliers using documented filters.
- Build surface/TIN with enforced breaklines and hydro-flattening where applicable.
- Produce contours at required interval; visually inspect for spikes, flat spots, and contour crossing.
- Populate metadata block: datums, projection, collection date, scale factor, geoid model, units.

### 4. QC review
- Run accuracy assessment: compute RMSEz and RMSEr from check shots or QA targets; target Class 1 (RMSEz ≤0.16 ft for 2 ft contours).
- Spot-check at least five random elevations and two contour paths against raw data.
- Verify that control notes, benchmarks, and coordinate tables exist in deliverables.
- Cross-check CSV point counts vs. CAD layers to confirm no data loss.

### 5. Delivery & retention
- Package PDF map, DWG/DXF, CSV points, TIN/LAS if requested, and metadata sheet.
- Ensure filenames and folder structure follow `Client_Project_Topo_v##`.
- Upload QC checklist, OPUS reports, and field logs to archive; retain for 7 years or state requirement.

## Accuracy & tolerance targets

| Element | Requirement |
|---------|-------------|
| Horizontal accuracy | ≤0.25 ft RMSE (ASPRS Class 1 1"=40' mapping) |
| Vertical accuracy | ≤0.16 ft RMSEz for 2 ft contours; adjust when finer contour interval required |
| Contour interval | Misclosure ≤0.5 x interval when compared to checkpoints |
| Breakline spacing | ≤25 ft (hardscape), ≤50 ft (natural) unless site dictates otherwise |

## Stage checklists

### Intake
- [ ] Control plan approved by PLS.
- [ ] Datum + projection recorded.
- [ ] Contour interval & deliverables documented.
- [ ] Site risks logged (vegetation, access, permits).

### Field
- [ ] Benchmarks observed twice and closure recorded.
- [ ] Weather/equipment logs uploaded.
- [ ] Redundant topo shots collected along grade breaks.
- [ ] Drone targets measured and tagged (if applicable).

### Processing/Drafting
- [ ] OPUS/RTK reports attached.
- [ ] Surface void map reviewed.
- [ ] Contour display checked for artifacts.
- [ ] Metadata block completed.

### QC & Delivery
- [ ] RMSE calculations documented.
- [ ] Spot elevation comparison signed by reviewer.
- [ ] Package validated (PDF, DWG, CSV, extras).
- [ ] Checklist archived with project.

## Nonconformance handling

- **Accuracy failure (RMSE exceeds tolerance):** Reprocess data, verify control, potentially recollect field data; QC lead must approve corrective action.
- **Missing features or gaps:** Return to drafter for completion; if data absent, PM coordinates supplemental field visit.
- **Datum/metadata errors:** Treat as major defect; update deliverables and issue corrected package with revision note.
- Track rework in QC metrics to refine training and partner selection.
