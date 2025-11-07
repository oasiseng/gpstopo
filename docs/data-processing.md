# Data Processing Workflow

GPSTopo converts raw field measurements into client-ready deliverables using a
standardized pipeline. Follow these steps to ensure repeatable, auditable
outputs regardless of the data source.

## 1. Ingestion

- Collect raw GPS, drone imagery, LiDAR point clouds, and field notes into the
  project staging area.
- Validate file integrity using checksums or spot checks before deleting media.
- Record dataset provenance in the project data log (source, date, operator,
  equipment, coordinate system).

## 2. Pre-Processing

- Normalize coordinate systems to the project datum using documented transforms.
- Clean and filter point data to remove outliers, signal dropouts, or noise.
- For imagery, apply radiometric corrections and align photo centers to the base
  coordinate system.
- Document any interpolations, smoothing, or adjustments in the processing log.

## 3. Modeling & Analysis

- Generate digital elevation models (DEMs), contours, and surfaces with software
  approved for the project scope.
- Conduct cross-checks between surfaces and control points to verify vertical and
  horizontal accuracy targets.
- Annotate analysis steps, including software versions, scripts, and parameters
  used to create the models.

## 4. Export & Packaging

- Export final datasets in required formats (e.g., DWG, DXF, GeoTIFF, CSV).
- Apply GPSTopo file naming conventions and embed metadata headers when
  supported.
- Update the QC checklist with processing-specific notes and outstanding items.

## 5. Handoff to Quality Control

- Submit processed data, logs, and project notes to the assigned reviewer.
- Archive intermediate files in `/Processing/YYYY/ProjectName/` with version
  tags.
- Flag any assumptions or data gaps so reviewers can address them during QC.

Consistent adherence to this workflow streamlines collaboration between field
teams, analysts, and project leads.
