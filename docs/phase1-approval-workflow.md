# Phase 1 Approval Workflow

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Define the approval path for Phase 1 content, assets, QA, and launch decisions.

## 1) Workflow Objective
- Prevent late-stage rework by sequencing approvals clearly.
- Ensure each approval has an owner, due date, and evidence.
- Tie all final decisions to launch go/no-go gates.

## 2) Approval Stages

| Stage | What Is Approved | Primary Approver | Secondary Reviewer | Exit Evidence |
|---|---|---|---|---|
| A1 | Wireframe structure and section order | Project Lead | Design/UX Lead | Updated `wireframe-phase1.md` |
| A2 | Placeholder copy direction | Content Lead | Project Lead | Updated `wireframe-copy-placeholders-phase1.md` |
| A3 | Media and proof assets | Content Lead | Compliance Lead | Approved rows in asset packet |
| A4 | CTA routing and tracking conventions | Ops Lead | Project Lead | Canonical URL + tracking standard documented |
| A5 | QA test pass for P1 cases | QA Lead | Launch Lead | `P1` tests marked `Pass` in QA matrix |
| A6 | Final launch decision | Launch Lead | Project Lead | Go/No-Go record in launch checklist |

## 3) Approval Matrix by Deliverable

| Deliverable | Required Approval Stage | Owner | Due Date | Status |
|---|---|---|---|---|
| `docs/wireframe-phase1.md` | A1 | [Assign] | [YYYY-MM-DD] | Open |
| `docs/wireframe-copy-placeholders-phase1.md` | A2 | [Assign] | [YYYY-MM-DD] | Open |
| `docs/phase1-asset-request-packet.md` | A3 | [Assign] | [YYYY-MM-DD] | Open |
| `docs/phase1-build-handoff-spec.md` | A4 | [Assign] | [YYYY-MM-DD] | Open |
| `docs/phase1-qa-test-case-matrix.md` | A5 | [Assign] | [YYYY-MM-DD] | Open |
| `docs/phase1-launch-readiness-checklist.md` | A6 | [Assign] | [YYYY-MM-DD] | Open |

## 4) SLA Targets
- Standard approval turnaround: 2 business days.
- `P1` blocked approvals escalation: within 24 hours of missed due date.
- Compliance-critical approvals: complete by T-72h before launch.

## 5) Escalation Rules
- If approver misses SLA, escalate to Project Lead.
- If compliance approval is pending at T-48h, launch status becomes `Conditional Go` at best.
- If any `P1` QA approval fails, launch status becomes `No-Go` until retest passes.

## 6) Approval Evidence Log

| Decision ID | Stage | Approved By | Date | Evidence Link | Notes |
|---|---|---|---|---|---|
| [APP-###] | [A#] | [Name] | [YYYY-MM-DD] | [Doc/Link] | [Notes] |

## 7) Weekly Review Actions
- Review all open approvals every Monday.
- Reconfirm due dates for `P1` approvals every Wednesday.
- Publish approval status in weekly update every Friday.

## 8) Related Docs
- `docs/phase1-decision-log.md`
- `docs/owner-assignment-sheet-phase1.md`
- `docs/phase1-launch-readiness-checklist.md`
- `docs/phase1-risk-register.md`
