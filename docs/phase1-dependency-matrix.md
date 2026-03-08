# Phase 1 Dependency Matrix

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Map critical dependencies between workstreams, deliverables, and milestones.

## 1) Dependency Types
- `Content`: copy, messaging, approvals
- `Asset`: media, logos, testimonials
- `Technical`: routing, tracking, implementation prerequisites
- `Operational`: team ownership, SLA, process readiness
- `Compliance`: legal or claims approvals

## 2) Dependency Matrix

| Dep ID | Type | Source Item | Depends On | Impacted Output | Owner | Due Date | Status | Risk if Delayed |
|---|---|---|---|---|---|---|---|---|
| D-001 | Content | Home Hero final copy | Content approval pass | Home build completion | [Assign] | [YYYY-MM-DD] | Open | CTA and above-fold trust impact |
| D-002 | Asset | Familiarity video section | Final video exports + captions | Home trust module | [Assign] | [YYYY-MM-DD] | Blocked | Reduced trust sequence quality |
| D-003 | Asset | Testimonial modules | Approved stories + consent | Home/Testimonial proof sections | [Assign] | [YYYY-MM-DD] | In Progress | Lower proof density at launch |
| D-004 | Technical | Apply CTA network | Canonical apply URL decision | Global CTA consistency + KPI attribution | [Assign] | [YYYY-MM-DD] | Open | Measurement and conversion ambiguity |
| D-005 | Technical | Contact form routing | Intent schema finalization | Contact and ops flow | [Assign] | [YYYY-MM-DD] | Open | Misrouted leads and delayed response |
| D-006 | Compliance | Claims copy across pages | Compliance approver signoff | Launch gate closure | [Assign] | [YYYY-MM-DD] | Open | Launch delay or rework risk |
| D-007 | Operational | Launch communications | Owner assignment confirmation | Launch coordination quality | [Assign] | [YYYY-MM-DD] | Open | Slower incident response |
| D-008 | QA | P1 test execution | Build completion + test mapping | Go/No-Go readiness | [Assign] | [YYYY-MM-DD] | Open | No validated launch confidence |

## 3) Dependency-to-Milestone Link

| Milestone | Critical Dependencies |
|---|---|
| M1 Structure Lock | D-001 |
| M2 Copy + Asset Baseline | D-001, D-002, D-003, D-006 |
| M3 P1 Build Complete | D-004, D-005 |
| M4 QA Pass Complete | D-008 |
| M5 Launch Decision | D-002, D-004, D-006, D-008 |

## 4) Escalation Rules
- Any dependency marked `Blocked` for >2 business days escalates to Project Lead.
- Any `Open` compliance dependency at T-48h triggers launch-risk review.
- Any unresolved technical dependency at T-24h triggers Conditional Go review.

## 5) Dependency Review Cadence
- Review every Wednesday blocker meeting.
- Reconfirm due dates every Friday dashboard update.
- Reflect status updates in risk register and weekly report.

## 6) Related Docs
- `docs/phase1-milestone-plan.md`
- `docs/phase1-work-package-map.md`
- `docs/phase1-risk-register.md`
- `docs/phase1-open-questions-register.md`
