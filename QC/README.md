# GPSTopo Quality Control Library

This folder consolidates service-specific quality control (QC) plans built for GPSTopo's licensed surveyor network. Each plan follows the same structure so project managers, drafters, and PLS reviewers can work from a shared mental model while still meeting the governing standards (PLS rules of practice, ALTA/NSPS 2021, ASPRS accuracy specs, FEMA guidance, and relevant ASTM/ACI references).

## How the QC plans are organized

Each service plan covers:
1. **Purpose & Scope** – why the service exists and what legal/industry expectations apply.
2. **Standards & References** – statutes, ASTM/ASPRS/ALTA requirements, and GPSTopo policies.
3. **Roles & Required Sign‑offs** – who owns each gate (PM, field partner, drafter, QC lead, PLS of record).
4. **QC Workflow** – five recurring phases: Pre‑Field Intake → Field Execution → Data Reduction & Drafting → QC Review → Delivery & Record Retention.
5. **Accuracy Targets & Checklists** – tolerance tables plus checkbox lists that mirror the process_qc_review.md workflow.
6. **Nonconformance Handling** – how to log defects, rework, and communicate with clients/partners.

Because the phases stay the same, teams can reuse muscle memory when switching services, while the embedded tolerances and references keep each deliverable compliant.

## Files in this folder

- `boundary_mapping.md`
- `topographic_survey.md`
- `construction_layout.md`
- `as_built_verification.md`
- `alta_nsps_survey.md`
- `custom_drone_mapping.md`

## Updating these plans

1. **Propose edits** via pull request referencing the service file.
2. **Tag the service owner** listed in gpstopo_business_spec.md and the QC lead.
3. **Link evidence** (field logs, client feedback, regulatory change).
4. **Document rollout** in process_main_order_workflow.md or automation docs if the change affects handoffs.

*Last updated: November 10, 2025 (update this stamp whenever material changes are approved).*
