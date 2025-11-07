# Quality Control Process

GPSTopo's quality assurance program ensures every deliverable reflects accurate
data, consistent presentation, and traceable approvals. The following phased
process must be followed for all client-facing outputs.

## 1. Data Verification

- Compare GPS, drone, or LiDAR data against known control points or benchmarks.
- Perform unit checks and confirm file naming conventions prior to processing.
- Review metadata completeness, including coordinate system, datum, equipment
  settings, and collection dates.
- Log anomalies or suspected issues in the project data log for follow-up.

## 2. Draft Review

- Assign an internal peer reviewer who was not the primary producer of the data.
- Validate units, elevations, contour spacing, symbology, and labeling against
  project requirements.
- Confirm that source data transformations (e.g., projections, smoothing) are
  documented and reproducible.
- Capture review notes in the QC checklist template and track outstanding items.

## 3. Final Review

- Project lead conducts a final sign-off using the QC checklist and attached
  reviewer notes.
- Ensure all deliverables are archived in `/Finals/YYYY/ProjectName/` with the
  approved version number and metadata snapshot.
- Confirm that any client-specific instructions or regulatory requirements are
  satisfied before release.

## 4. Version Control

- Track updates through Git commit history or managed cloud revision logs.
- Apply version naming pattern `vYYYY.MM.DD-Initials` (e.g., `v2025.03.12-JD`).
- Retain prior versions for auditability and rollbacks.
- Document major changes in the project changelog or repository release notes.

By adhering to these steps, GPSTopo maintains defensible data integrity and
delivers consistent value across projects.
