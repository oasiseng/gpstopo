# Client Delivery Standards

GPSTopo packages deliverables with consistent structure, metadata, and visual
branding. Follow this checklist before transmitting files to clients.

## File Naming Conventions

- Use descriptive, versioned filenames such as `ProjectName_Topo_v1.pdf`,
  `ProjectName_Points_v1.csv`, and `ProjectName_Surface_v1.dwg`.
- Increment version numbers when revisions are issued, maintaining a change log
  in the project folder.
- Group deliverables into folders by type (e.g., `PDF`, `CAD`, `CSV`) to simplify
  client navigation.

## PDF Layout Standards

- Include the GPSTopo logo, project title block, north arrow, scale bar, and
  coordinate system reference.
- Present a conspicuous disclaimer stating that GPSTopo does not provide legal
  land-surveying services and that licensed surveyors must verify boundaries
  where required.
- Ensure contours, spot elevations, and annotations use GPSTopo standard colors
  and line weights.
- Add a revision table summarizing version, date, and reviewer initials.

## Required Metadata

- Embed the following metadata in each file or provide a companion README:
  - Project name and location (general description, no client-sensitive data).
  - Collection dates and equipment used.
  - Coordinate reference system and vertical datum.
  - Accuracy statements and known limitations.
- Provide a `deliverable_summary.md` or PDF that outlines contents, coordinate
  systems, and contact information for follow-up.

## Delivery & Archiving

- Package files into a compressed archive with checksum documentation when
  possible.
- Upload to the approved delivery platform (e.g., secure cloud share) and
  confirm client access.
- Store a copy in `/Finals/YYYY/ProjectName/` along with QC checklists and
  correspondence confirming receipt.
- Notify the client with a clear summary of deliverables, access instructions,
  and support contact details.

Adhering to these standards reinforces GPSTopo's professional presentation and
ensures clients can rely on our deliverables for their project decisions.
