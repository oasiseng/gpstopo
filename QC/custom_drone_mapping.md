# Custom Drone / LiDAR Mapping QC Plan

## Purpose & scope

Produce aerial photogrammetry or LiDAR datasets (orthomosaics, point clouds, DSM/DTM models) for larger or complex sites. QC ensures data meets positional accuracy targets, is compliant with FAA Part 107 rules, and integrates seamlessly with GPSTopo downstream deliverables.

## Governing standards & references

- FAA Part 107 regulations (pilot certification, airspace authorization, operations over people).
- ASPRS Positional Accuracy Standards for Digital Geospatial Data (2023) – lidar/imagery classes.
- USGS Lidar Base Specification v2.1 (or newest) for point density, classification, and metadata.
- FGDC Standards for Geospatial Metadata (FGDC-STD-014-2002).
- State privacy or UAS-specific regulations.

## Roles & sign-offs

| Stage | Owner | QC gate |
|-------|-------|---------|
| Mission planning | UAS Coordinator + PM | Airspace & ground control plan approved |
| Flight operations | Remote Pilot in Command (RPIC) | Daily flight log & safety checklist |
| Data processing | Geospatial Specialist | Software QA (bundle adjustment, classification) |
| Technical QC | QC Lead (PLS/PE/ASPRS-certified) | Accuracy report + deliverable review |
| Delivery | PM | Client package + metadata release |

## QC workflow

### 1. Mission planning
- Define deliverables (orthomosaic, DSM/DTM, contours, volumetrics) and accuracy class required.
- Obtain airspace authorization (LAANC or FAA waiver) and landowner permissions.
- Design flight plan (altitude, sidelap/overlap, speed) to achieve Ground Sample Distance (GSD) that supports target accuracy.
- Plan ground control points (GCPs) and checkpoints; minimum 5 distributed GCPs plus checkpoints equal to 10% of GCP count.

### 2. Flight operations
- Conduct pre-flight inspection (airframe, sensors, batteries); log results.
- Deploy GCPs with survey-grade observations tied to project datum; record photos and descriptions.
- Capture raw imagery/LiDAR with time stamps and IMU data; monitor for blur, motion artifacts, or GNSS dropouts.
- Complete post-flight log including file counts, issues, and weather.

### 3. Data processing
- Import data into photogrammetry/LiDAR software (Pix4D, Metashape, Terrasolid, etc.) with calibrated camera parameters.
- Apply GCPs/checkpoints; review residuals (target ≤0.05 ft XY, ≤0.10 ft Z for Class I).
- Filter noise, classify ground/non-ground, and enforce breaklines if needed.
- Generate deliverables (orthomosaic GeoTIFF, LAS/LAZ, DEM/DSM, contours) and QA for seamlines, voids, color balance.
- Populate metadata (projection, datums, acquisition date, sensor, processing version).

### 4. Technical QC
- Evaluate accuracy report: RMSE, NSSDA statistics, point density, coverage completeness.
- Visually inspect point cloud cross-sections and hillshades for artifacts.
- Verify tile indexing, file sizes, and naming per GPSTopo conventions.
- Ensure deliverables integrate with CAD/GIS environment (test load in Civil 3D/QGIS).

### 5. Delivery & retention
- Package orthomosaic, point cloud, DEM/DSM, contour files, metadata PDF, accuracy report, and flight logs.
- Upload to client portal/cloud storage with checksum or hash for integrity.
- Retain raw imagery, flight logs, processing projects, and QC results for minimum 5 years.

## Accuracy & tolerance targets

| Class | Horizontal RMSE | Vertical RMSE | Notes |
|-------|-----------------|---------------|-------|
| Class I (design-grade) | ≤0.08 ft | ≤0.10 ft | Requires surveyed GCPs/checkpoints |
| Class II (planning-grade) | ≤0.20 ft | ≤0.25 ft | Fewer GCPs acceptable but checkpoints still required |

Point density: ≥100 pts/m² for LiDAR or ≥2 cm GSD imagery for Class I deliverables (adjust per scope).

## Stage checklists

### Mission planning
- [ ] Airspace authorization secured.
- [ ] GCP/checkpoint layout approved by PLS.
- [ ] Weather and logistics reviewed 24 hrs prior.
- [ ] Client deliverables/accuracy expectations documented.

### Flight
- [ ] Pre-flight checklist signed.
- [ ] GCPs surveyed and photographed.
- [ ] Flight logs uploaded same day.
- [ ] Any anomalies (wind, GPS, obstructions) documented.

### Processing/QC
- [ ] Bundle adjustment residuals within tolerance.
- [ ] Accuracy report generated and stored.
- [ ] Visual QA (cross-sections, hillshade) completed.
- [ ] Deliverables validated in downstream software.

## Nonconformance handling

- **Accuracy failure:** Reprocess with refined calibration or weighting; if still out of tolerance, schedule reflight. Document root cause (control error, weather, sensor issue).
- **Data gaps or artifacts:** Classify severity; patch with supplemental flights or note limitation in deliverable if client approves.
- **Regulatory issue (airspace violation, missing waiver):** Immediately notify compliance officer; halt deliveries until resolved and document corrective action.
- Track drone partner performance (mission success rate, rework hours) to inform vendor selection.
