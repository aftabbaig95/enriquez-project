# Phase 1 Program Handbook

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Consolidated operator guide for executing Phase 1 from planning through launch and transition.

## 1) Program Mission
Deliver a trust-centered, conversion-focused Phase 1 website experience that supports:
- Business-owner funding inquiries
- ISO partner inquiries

Program outcomes:
- Clear page hierarchy and CTA routing
- Stronger proof sequence and trust architecture
- Launch governance and reporting discipline

## 2) Program Structure
- Lane A: Visual/UX/Branding
- Lane B: Functional Features (planning boundary in Phase 1)
- Lane C: Backend/Operations (planning boundary in Phase 1)

Core principle:
- Treat lane scope independently to avoid hidden complexity and scope bleed.

## 3) Execution Lifecycle
1. Structure lock
2. Copy and asset lock
3. Build execution
4. QA and hardening
5. Go/No-Go decision
6. Launch and stabilization
7. Completion and Phase 2 transition

## 4) Source of Truth Docs

### Strategy and Scope
- `docs/scope-phases.md`
- `docs/sitemap.md`
- `docs/audit.md`

### Design and Content
- `docs/wireframe-phase1.md`
- `docs/wireframe-copy-placeholders-phase1.md`
- `docs/content-production-tracker-phase1.md`

### Execution and Ownership
- `docs/phase1-work-package-map.md`
- `docs/phase1-milestone-plan.md`
- `docs/phase1-raci-matrix.md`
- `docs/owner-assignment-sheet-phase1.md`

### Launch Governance
- `docs/phase1-launch-readiness-checklist.md`
- `docs/phase1-launch-day-runbook.md`
- `docs/phase1-launch-communications-plan.md`
- `docs/phase1-qa-test-case-matrix.md`

### Reporting and Controls
- `docs/phase1-weekly-execution-dashboard.md`
- `docs/phase1-kpi-weekly-report-template.md`
- `docs/phase1-risk-register.md`
- `docs/phase1-open-questions-register.md`
- `docs/phase1-change-request-log.md`

## 5) Operating Rhythm

### Daily
- Run standup using `phase1-daily-standup-script.md`.
- Update action register and tracker statuses.

### Weekly
- Monday: owner/status alignment.
- Wednesday: blocker and dependency triage.
- Friday: dashboard, KPI report, and stakeholder update.

### Pre-Launch
- Run launch-readiness checklist.
- Confirm QA `P1` pass status.
- Confirm communications and rollback owners.

## 6) Governance Rules
- Every `P1` item must have owner + due date.
- No unlogged scope changes; use change-request log.
- No launch if any critical gate is blocked.
- Keep master index current for every new artifact.

## 7) Escalation Model
- `P1` blocker >1 business day: escalate to Project Lead.
- Compliance unresolved at T-48h: launch risk escalation.
- CTA routing unresolved at T-24h: Conditional Go/No-Go review.
- `P1` QA fail at decision point: No-Go until resolved.

## 8) Program Health Indicators
- Readiness score >= target band.
- Risk profile trending from Elevated/Critical to Moderate/Low.
- `P1` approval and QA pass rates improving week over week.
- Open-question count trending down.

## 9) Closeout and Transition
- Complete `phase1-completion-report-template.md`.
- Carry forward unresolved items into `phase2-transition-brief-template.md`.
- Preserve dated dashboard/report snapshots for audit trail.

## 10) Quick Start for New Operator
- Read `phase1-implementation-brief.md`.
- Read `phase1-onboarding-quickstart.md`.
- Review `phase1-master-index.md`.
- Claim one `P1` action with due date and update action register.
