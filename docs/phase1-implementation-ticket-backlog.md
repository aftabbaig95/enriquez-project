# Phase 1 Implementation Ticket Backlog

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Translate Phase 1 planning artifacts into execution-ready ticket stubs.

## 1) Usage
- One row equals one implementation ticket.
- Keep acceptance criteria directly tied to wireframe/build docs.
- Assign priority and owner before sprint kickoff.

## 2) Ticket Backlog

| Ticket ID | Priority | Epic | Title | Description | Acceptance Criteria | Dependencies | Owner | Status |
|---|---|---|---|---|---|---|---|---|
| WF-001 | P1 | Home | Build Home page section structure | Implement Home sections in approved order from wireframe doc | Section order matches `wireframe-phase1.md`; no required section missing | None | [Assign] | Ready |
| WF-002 | P1 | Home | Wire Hero and Final CTA routes | Connect hero/final apply CTAs to canonical apply path | Both CTAs pass QA-001 and QA-002 | Canonical apply URL finalized | [Assign] | Blocked |
| WF-003 | P1 | Home | Add FAQ objection module | Implement FAQ block and mobile accordion behavior | FAQ questions render clearly; mobile readable; passes QA-202 | Copy finalized | [Assign] | Ready |
| WF-004 | P1 | ISO | Build ISO page structure | Implement ISO sections and partner-first flow | ISO order matches wireframe; partner differentiation clear | None | [Assign] | Ready |
| WF-005 | P1 | ISO | Integrate partner media modules | Add partner visit media blocks with labels | All location modules render; no missing media references | Video assets validated | [Assign] | Blocked |
| WF-006 | P1 | Testimonials | Build testimonials proof layout | Implement featured stories and quote grid section blocks | Proof content visible before conversion prompt | Testimonial assets approved | [Assign] | In Progress |
| WF-007 | P1 | Contact | Build contact cards + form | Implement contact cards and intent-routed form | Contact cards verified; form supports Funding/ISO/General intent | Contact details confirmed | [Assign] | Ready |
| WF-008 | P1 | Apply Entry | Build apply entry handoff page | Implement apply intro, checklist, and support prompt | Apply handoff works; support CTA visible near handoff | Canonical apply URL finalized | [Assign] | Ready |
| WF-009 | P2 | Company Principles | Build light principles page | Implement principles hero, values, commitment sections | Page includes trust narrative + CTA | Final principles copy | [Assign] | Not Started |
| WF-010 | P2 | Resources | Build resources shell page | Implement resources hero, teaser, and modules | Page clearly marks phase 2 tools as coming soon | Placeholder assets | [Assign] | Not Started |
| WF-011 | P1 | Global QA | Execute P1 QA matrix pass | Run all P1 test cases and log defects | No P1 test remains Fail/Blocked at go/no-go | Implementation complete | [Assign] | Not Started |
| WF-012 | P1 | Launch | Execute launch-day runbook | Run cutover and smoke-test sequence | T+15 and T+45 smoke tests pass | Go decision approved | [Assign] | Not Started |

## 3) Sprint Packaging Suggestion
- Sprint A (P1 build): WF-001, WF-004, WF-006, WF-007, WF-008
- Sprint B (P1 hardening): WF-002, WF-003, WF-005, WF-011
- Launch window: WF-012
- Post-launch: WF-009, WF-010

## 4) Definition of Ticket Done
- Acceptance criteria met.
- Related QA test IDs pass.
- Linked dependency status is not `Blocked`.
- Owner updates tracker and weekly report.

## 5) Related Docs
- `docs/phase1-build-handoff-spec.md`
- `docs/phase1-qa-test-case-matrix.md`
- `docs/content-production-tracker-phase1.md`
- `docs/phase1-launch-day-runbook.md`
