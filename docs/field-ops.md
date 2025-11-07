# Field Operations Guide

This guide defines GPSTopo's expectations for safe, consistent, and auditable
field data collection. Every crew member is responsible for reviewing these
procedures before mobilizing to a site.

## Equipment Setup Checklist

1. Inspect all GPS/RTK units, drones, batteries, and controllers for damage.
2. Confirm firmware and software versions are up to date.
3. Verify spare batteries, memory cards, and backup media are available.
4. Calibrate tripod and pole levels; inspect tribrachs and prisms.
5. Pack personal protective equipment (PPE) appropriate to the job site.
6. Review project-specific hazards and emergency contacts.

Record completion of the checklist in the field log before departure.

## RTK Calibration Verification

- Establish the base station on a known control point where possible.
- Log start and end times, coordinates, and antenna heights for base sessions.
- Perform a two-point check using independent benchmarks to confirm reported
  precision is within tolerance.
- Document environmental factors (weather, multipath risks, obstructions) that
  could influence signal quality.
- If tolerances exceed project limits, halt data collection and troubleshoot or
  escalate to the project lead.

## Drone Mission Setup & Data Logging

- Review airspace restrictions, NOTAMs, and site-specific flight permissions.
- Configure mission parameters (altitude, overlap, speed) according to project
  deliverables and regulatory requirements.
- Conduct a pre-flight checklist: IMU calibration, compass check, propeller
  inspection, return-to-home altitude, and failsafe behavior.
- Assign a visual observer when required by regulation or site complexity.
- Start a mission log capturing battery cycles, flight durations, image counts,
  and any anomalies encountered.
- Immediately after landing, back up imagery to two locations and verify file
  integrity before leaving the site.

## Naming Conventions & Data Handoff

- Use the format `ProjectName_Area_Date_Dataset` for raw data folders.
- Name individual files with incremental numbering (e.g., `SiteA_RTLog_2025-03-18.csv`).
- Upload raw datasets to the designated staging area within 24 hours.
- Submit the completed field log and any incident reports to the project lead.

Consistent documentation preserves traceability and enables reliable downstream
processing for every GPSTopo project.
