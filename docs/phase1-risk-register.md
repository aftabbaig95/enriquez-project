# Phase 1 Risk Register

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Maintain a live risk register for Phase 1 launch planning and execution.

## 1) Scoring Model
- Probability: `Low`, `Medium`, `High`
- Impact: `Low`, `Medium`, `High`
- Score guidance:
  - High + High = Critical
  - Any High + Medium = Elevated
  - Medium + Medium = Moderate

## 2) Risk Register

| Risk ID | Category | Risk Statement | Probability | Impact | Current Rating | Mitigation Plan | Trigger | Owner | Status |
|---|---|---|---|---|---|---|---|---|---|
| R-001 | Content/Assets | Launch-critical media (team/partner videos) is not ready in time | High | High | Critical | Define minimum launch-safe asset set; escalate blocked assets within 24h | `P1` media still `Blocked` at T-48h | [Assign] | Open |
| R-002 | Conversion | Apply CTAs route to inconsistent destinations | Medium | High | Elevated | Enforce canonical apply URL and review all CTA links in QA matrix | Any CTA points to non-canonical endpoint | [Assign] | Open |
| R-003 | Operations | Contact intent routing is unclear, causing delayed follow-up | Medium | High | Elevated | Add/validate intent field and assign ops owner for triage | Funding/ISO inquiries not routed correctly in test | [Assign] | Open |
| R-004 | Compliance | Claims language requires late rework due to missing review | Medium | High | Elevated | Schedule compliance pass before content lock | Compliance signoff missing at T-72h | [Assign] | Open |
| R-005 | QA | Critical defects discovered during launch window | Low | High | Elevated | Execute staged QA + smoke tests; pre-assign rollback owner | Any `P1` QA case fails at T-0 | [Assign] | Open |
| R-006 | Timeline | Unassigned owners delay approvals and delivery | Medium | Medium | Moderate | Populate owner assignment sheet and due dates for all `P1` rows | `P1` rows still unassigned after weekly review | [Assign] | Open |
| R-007 | Tracking | Missing tracking standards prevents attribution visibility | Medium | Medium | Moderate | Define tagging convention and verify with QA-301/302 | Campaign/source cannot be identified post-launch | [Assign] | Open |
| R-008 | Platform | Last-minute platform constraints block intended behavior | Low | Medium | Moderate | Confirm constraints early and document fallback options | Required component cannot be implemented as spec'd | [Assign] | Monitoring |

## 3) Weekly Risk Review
- Review `Critical` and `Elevated` risks first.
- Re-score risks after mitigation changes.
- Move resolved risks to `Closed` with closure date and evidence.

## 4) Escalation Rules
- Any `Critical` risk at T-72h to launch: escalate to Launch Lead and decision owners.
- Any risk with missed mitigation due date: escalate in weekly stakeholder update.
- Any unresolved compliance risk at T-48h: force `Conditional Go` or `No-Go` decision.

## 5) Closure Log

| Risk ID | Closure Date | Closed By | Closure Evidence |
|---|---|---|---|
| [R-###] | [YYYY-MM-DD] | [Name] | [Link or note] |

## 6) Linked Docs
- `docs/phase1-launch-readiness-checklist.md`
- `docs/phase1-launch-day-runbook.md`
- `docs/phase1-qa-test-case-matrix.md`
- `docs/owner-assignment-sheet-phase1.md`
- `docs/weekly-update-2026-03-07.md`
