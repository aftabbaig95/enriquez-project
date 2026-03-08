# Phase 1 Document Maintenance Policy

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Keep planning and launch documents accurate, current, and auditable.

## 1) Policy Objectives
- Prevent stale planning data from driving execution.
- Ensure changes are reflected in the correct control documents.
- Maintain traceability for approvals, risks, and decisions.

## 2) Update Frequency by Document Type

| Document Type | Examples | Minimum Update Frequency | Owner Role |
|---|---|---|---|
| Daily execution docs | Action register, standup script notes | Daily on workdays | Project Lead |
| Weekly governance docs | Dashboard, KPI report, stakeholder update | Weekly (Friday) | Project Lead |
| Risk/issue controls | Risk register, open questions, change log | At least 2x weekly + on major event | Project Lead |
| Launch controls | Readiness checklist, runbook, QA matrix | Before each launch checkpoint | Launch Lead / QA Lead |
| Structural docs | Wireframe, build handoff, milestone plan | On approved changes only | UX/Build Leads |

## 3) Change Propagation Rules
- If CTA routing changes, update:
  - Build handoff spec
  - QA matrix
  - Launch readiness checklist
  - KPI tracking references
- If a blocker is resolved, update:
  - Action register
  - Risk register
  - Open questions register (if applicable)
- If scope changes, update:
  - Change request log
  - Decision log
  - Master index references (if new doc added)

## 4) Master Index Governance
- Every new Phase 1 artifact must be added to `phase1-master-index.md`.
- Include a short purpose description for new entries.
- Keep sections grouped by `Start Here`, `Wireframe Core`, `Production Management`, `Launch Controls`.

## 5) Quality Checks Before Marking a Doc "Current"
- Owner and date fields are present.
- Links to related docs are valid.
- Status values are consistent with tracker and dashboard.
- Placeholder fields are minimized for active execution docs.

## 6) Archival and Versioning
- Keep dated snapshots for weekly dashboards/reports.
- Do not overwrite historical weekly reports.
- Use new dated files for major weekly cycles.

## 7) Compliance and Audit Trace
- Ensure approval evidence is recorded in approval workflow log.
- Ensure decision outcomes are captured in decision log.
- Ensure all major launch decisions have date + owner recorded.

## 8) Related Docs
- `docs/phase1-master-index.md`
- `docs/phase1-approval-workflow.md`
- `docs/phase1-change-request-log.md`
- `docs/phase1-weekly-execution-dashboard.md`
