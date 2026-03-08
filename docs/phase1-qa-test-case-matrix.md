# Phase 1 QA Test Case Matrix

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Define repeatable QA tests for Phase 1 page builds before go/no-go.

## 1) Test Status Key
- `Not Run`
- `Pass`
- `Fail`
- `Blocked`

## 2) Test Priority Key
- `P1`: Launch-critical, must pass.
- `P2`: High-value quality check, fix before full rollout where possible.
- `P3`: Non-blocking enhancement check.

## 3) Functional CTA Tests

| Test ID | Priority | Page | Test Case | Steps | Expected Result | Status | Owner | Notes |
|---|---|---|---|---|---|---|---|---|
| QA-001 | P1 | Home | Hero Apply CTA | Click hero `Apply Now` | Opens canonical apply destination | Not Run | [Assign] | |
| QA-002 | P1 | Home | Final CTA Apply | Click final apply CTA | Opens canonical apply destination | Not Run | [Assign] | |
| QA-003 | P1 | ISO | Partner Apply CTA | Click partner apply CTA | Opens intended partner apply flow | Not Run | [Assign] | |
| QA-004 | P1 | Testimonials | Conversion CTA | Click final testimonials CTA | Routes to canonical apply path | Not Run | [Assign] | |
| QA-005 | P1 | Contact | Contact form submit | Complete required fields + submit | Submission succeeds and route intent captured | Not Run | [Assign] | |
| QA-006 | P1 | Apply Entry | Handoff CTA | Click continue/apply CTA | External handoff opens correctly | Not Run | [Assign] | |
| QA-007 | P1 | Global | Phone CTA behavior | Tap phone CTA on mobile | Device initiates call intent | Not Run | [Assign] | |

## 4) Content and Structure Tests

| Test ID | Priority | Page | Test Case | Steps | Expected Result | Status | Owner | Notes |
|---|---|---|---|---|---|---|---|---|
| QA-101 | P1 | Home | Section order validation | Compare page to wireframe order | Matches approved sequence in `wireframe-phase1.md` | Not Run | [Assign] | |
| QA-102 | P1 | ISO | Section order validation | Compare page to wireframe order | Matches approved sequence in `wireframe-phase1.md` | Not Run | [Assign] | |
| QA-103 | P1 | Testimonials | Proof-first hierarchy check | Review section prominence | Proof modules are dominant before final CTA | Not Run | [Assign] | |
| QA-104 | P1 | Contact | Intent clarity check | Review copy in hero/form | Funding vs ISO intent is explicit | Not Run | [Assign] | |
| QA-105 | P2 | Global | CTA naming consistency | Review CTA labels across pages | Primary CTA uses consistent naming (`Apply Now`) | Not Run | [Assign] | |
| QA-106 | P2 | Global | Footer consistency | Check footer links on all pages | Privacy/compliance/contact links are consistent | Not Run | [Assign] | |

## 5) Responsive and Accessibility-Oriented Checks

| Test ID | Priority | Scope | Test Case | Steps | Expected Result | Status | Owner | Notes |
|---|---|---|---|---|---|---|---|---|
| QA-201 | P1 | Mobile | CTA visibility | Review on small viewport | Primary CTA is visible and usable | Not Run | [Assign] | |
| QA-202 | P1 | Mobile | Content readability | Review key sections on mobile | No clipped text or unusable spacing | Not Run | [Assign] | |
| QA-203 | P2 | Global | Keyboard navigation | Tab through nav + CTA + form fields | Focus order is logical and complete | Not Run | [Assign] | |
| QA-204 | P2 | Global | Form input clarity | Inspect labels/placeholders/errors | Inputs and validation messages are clear | Not Run | [Assign] | |

## 6) Tracking and Attribution Tests

| Test ID | Priority | Scope | Test Case | Steps | Expected Result | Status | Owner | Notes |
|---|---|---|---|---|---|---|---|---|
| QA-301 | P1 | CTA links | Tracking parameter presence | Inspect CTA destinations | Required tracking parameters are present | Not Run | [Assign] | |
| QA-302 | P1 | Apply path | Apply source attribution | Complete test click path | Source data can be attributed by path | Not Run | [Assign] | |
| QA-303 | P2 | Contact path | Contact intent tagging | Submit each intent category | Routing tags reflect selected intent | Not Run | [Assign] | |

## 7) Defect Log

| Defect ID | Severity | Related Test ID | Summary | Owner | Status | Target Fix Date |
|---|---|---|---|---|---|---|
| [DEF-###] | [Critical/Major/Minor] | [QA-###] | [Summary] | [Assign] | Open | [YYYY-MM-DD] |

## 8) Go/No-Go QA Rule
- `No-Go` if any `P1` test is `Fail` or `Blocked` at decision time.
- `Conditional Go` allowed only for `P2/P3` failures with documented mitigation and owner.

## 9) Related Docs
- `docs/phase1-build-handoff-spec.md`
- `docs/phase1-launch-readiness-checklist.md`
- `docs/phase1-launch-day-runbook.md`
- `docs/content-production-tracker-phase1.md`
