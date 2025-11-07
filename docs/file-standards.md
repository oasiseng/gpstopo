# File Standards & Version Control

Standardizing file formats and revision practices enables GPSTopo to collaborate
smoothly across teams and tools.

## Format Requirements

- **CAD**: Deliver final CAD drawings in DWG (2018) format with accompanying DXF
  exports when clients request open standards. Include XREFs in a `/xref/`
  subfolder.
- **Raster**: Provide GeoTIFF or JPEG2000 imagery with embedded spatial
  reference information.
- **Point Data**: Export CSV or LAS/LAZ files with headers describing coordinate
  system, units, and attribute fields.
- **Reports**: Publish PDFs with bookmarks, table of contents, and embedded
  fonts for portability.

## Naming & Organization

- Apply the folder hierarchy `ProjectName/DataType/Version/` for active work.
- Use lowercase, hyphenated filenames where possible (e.g.,
  `site-a-control-network_v2025.03.18-jd.dwg`).
- Store reference materials (field notes, photos) in `/Reference/` with matching
  identifiers to processed outputs.

## Version Control Practices

- Tag major milestones using the `vYYYY.MM.DD-Initials` convention.
- Capture change summaries in `CHANGELOG.md` or the project changelog file.
- Avoid overwriting prior versions; archive superseded files in `/Archive/` with
  a readme describing why the version was replaced.
- Leverage Git LFS or cloud storage for large binary files and document the
  storage location in repository notes.

## Quality Flags

- Prefix files under review with `_DRAFT` and remove the flag after approval.
- Append `_HOLD` to files paused for client feedback and note the reason in the
  QC checklist.
- Maintain a `README` in each project folder explaining the current status of
  files and open tasks.

These standards promote clarity and reduce the risk of miscommunication during
project handoffs.
