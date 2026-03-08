# Phase 1 Launch Day Runbook

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Step-by-step execution plan for launch day.

## 1) Runbook Scope
- Applies to Phase 1 launch pages and core CTA flows.
- Covers final pre-launch checks, cutover actions, post-launch validation, and rollback triggers.
- Use with:
  - `docs/phase1-launch-readiness-checklist.md`
  - `docs/owner-assignment-sheet-phase1.md`
  - `docs/content-production-tracker-phase1.md`

## 2) Launch Team Roles

| Role | Primary Responsibility | Assigned To | Backup |
|---|---|---|---|
| Launch Lead | Own go/no-go decision and timeline control | [Assign] | [Assign] |
| Content Lead | Validate final copy and media placement | [Assign] | [Assign] |
| QA Lead | Execute test scripts and report defects | [Assign] | [Assign] |
| Tracking Lead | Confirm CTA and tracking integrity | [Assign] | [Assign] |
| Ops Lead | Confirm follow-up readiness and escalation handling | [Assign] | [Assign] |
| Rollback Lead | Execute rollback if trigger criteria met | [Assign] | [Assign] |

## 3) T-24 Hours Checklist
- Confirm all critical gates in `docs/phase1-launch-readiness-checklist.md` are `Done`.
- Freeze launch copy and media asset set.
- Confirm canonical Apply URL and tracking convention.
- Confirm contact details and response-time statement.
- Confirm escalation channel and launch-day communication thread.

## 4) Launch-Day Timeline (Suggested)

### T-90 Minutes: Final Readiness Review
- Launch Lead runs 10-minute gate review.
- Confirm no open blockers in critical gates.
- Verify owners are present and reachable.

### T-60 Minutes: Final QA Pass (Staging or Preview)
- QA Lead verifies:
  - Primary nav links.
  - Hero and final CTA links.
  - Apply handoff path.
  - Contact form submission and routing behavior.
  - Mobile CTA behavior on at least one iOS and one Android viewport.
- Log any defects with severity labels: `Critical`, `Major`, `Minor`.

### T-30 Minutes: Content and Tracking Lock
- Content Lead confirms final copy/media match approved set.
- Tracking Lead validates URL tags and CTA destinations.
- Launch Lead confirms go/no-go recommendation.

### T-0: Launch Cutover
- Execute publish action.
- Record exact launch timestamp.
- Announce "Launch Complete - Monitoring" in team channel.

### T+15 Minutes: Smoke Test Round 1
- QA Lead runs smoke checks on live site:
  - Home hero CTA.
  - ISO hero CTA.
  - Testimonials CTA.
  - Contact form submit.
  - Apply entry handoff.
- Confirm no broken links or critical rendering issues.

### T+45 Minutes: Smoke Test Round 2 (Cross-device)
- Repeat CTA and form checks on desktop + mobile.
- Validate contact tap-to-call behavior.
- Confirm key pages load and footer links resolve.

### T+90 Minutes: Operational Validation
- Ops Lead confirms inbound paths are functioning:
  - Application starts received.
  - Contact requests visible to follow-up owner.
  - No routing dead ends.

### T+120 Minutes: Stabilization Checkpoint
- Review incidents raised in first two hours.
- Decide: `Stable` or `Needs rollback/patch`.
- Document final launch-day status.

## 5) Smoke Test Script

| Test ID | Test Case | Expected Result | Owner | Status | Notes |
|---|---|---|---|---|---|
| S1 | Home `Apply Now` CTA | Opens canonical Apply endpoint | [Assign] | Open | |
| S2 | Home secondary CTA | Routes to intended destination | [Assign] | Open | |
| S3 | ISO `Partner Apply` CTA | Opens partner apply path | [Assign] | Open | |
| S4 | Testimonials CTA | Routes to canonical Apply endpoint | [Assign] | Open | |
| S5 | Contact form submit | Submission succeeds and routes correctly | [Assign] | Open | |
| S6 | Contact direct cards | Phone/email actions function correctly | [Assign] | Open | |
| S7 | Apply entry handoff | External handoff opens and returns as expected | [Assign] | Open | |
| S8 | Privacy/compliance links | All utility links resolve correctly | [Assign] | Open | |
| S9 | Mobile sticky CTA | Visible and tappable on mobile viewport | [Assign] | Open | |
| S10 | CTA tracking tags | Tracking params are present and consistent | [Assign] | Open | |

## 6) Incident Severity Model
- `Critical`: Primary conversion path broken (Apply, Contact, or routing). Immediate rollback decision required.
- `Major`: Significant UX break affecting trust/CTA clarity. Fix within same launch window.
- `Minor`: Non-blocking copy/layout issues. Queue for next update window.

## 7) Rollback Triggers
Immediate rollback if any of the following occur:
- Primary Apply path fails consistently.
- Contact submission path is broken.
- Critical legal/compliance error is discovered.
- Multiple `Critical` issues remain unresolved after 30 minutes.

## 8) Rollback Procedure
1. Launch Lead declares rollback and notifies team.
2. Rollback Lead reverts to prior stable version.
3. QA Lead validates restored baseline paths.
4. Ops Lead confirms inbound handling is stable.
5. Launch Lead sends status update with root cause and next-attempt plan.

## 9) Communication Templates

### Launch Start
"Phase 1 launch is now in progress. Cutover timestamp: [time]. Monitoring window is active."

### Stable Update
"Phase 1 launch is stable after smoke tests. Core CTA and contact paths are functioning as expected."

### Incident Update
"Issue detected: [summary]. Severity: [Critical/Major/Minor]. Owner: [name]. ETA: [time]."

### Rollback Notice
"Rollback initiated due to [reason]. Team is restoring prior stable version and will share next update at [time]."

## 10) Post-Launch (Day +1)
- Record launch metrics baseline:
  - Application starts.
  - Contact submissions.
  - CTA click-through by page.
- Review all incidents and resolutions.
- Open follow-up tasks for deferred `Minor` items.
- Update next weekly stakeholder report with launch outcomes.
