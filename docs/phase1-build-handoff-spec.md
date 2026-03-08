# Phase 1 Build Handoff Spec

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Convert wireframe outputs into implementation-ready page requirements.

## 1) Scope
This handoff spec covers Phase 1 page builds only:
- Home
- ISO Partnerships
- Testimonials
- Contact
- Apply Entry
- Company Principles (light)
- Resources (light shell)

Out of scope for this spec:
- Calculator logic implementation
- CRM/workflow automation implementation
- Advanced backend integrations

## 2) Global Requirements

### Navigation
- Header includes: Home, ISO Partnerships, Testimonials, Resources, Company Principles, Contact.
- Primary global CTA: `Apply Now`.
- Mobile includes persistent CTA behavior consistent with wireframe intent.

### Footer
- Include contact methods, social links, privacy/compliance links.
- Ensure consistency across all core pages.

### CTA Rules
- Canonical Apply destination used for all primary apply CTAs.
- CTA label consistency: `Apply Now` as primary naming pattern.
- Secondary CTA (where present): `Call Team` or equivalent direct contact action.

### Content Rules
- Use placeholders from `docs/wireframe-copy-placeholders-phase1.md` until final approved copy is delivered.
- Keep section ordering aligned with `docs/wireframe-phase1.md` unless explicitly approved in decision log.

## 3) Page Build Requirements

### Home
Required sections (in order):
1. Header/Nav
2. Hero (primary + secondary CTA)
3. Familiarity Video Block
4. Value Pillars
5. Credibility Strip
6. Funding Outcomes
7. Testimonial Preview
8. FAQ/Objection Handling
9. Process Overview
10. Tool Teaser
11. Final CTA
12. Footer

Minimum acceptance:
- Hero and final CTA both route correctly.
- FAQ section supports clear question/answer readability.
- At least one proof module is visible above lower-page conversion prompts.

### ISO Partnerships
Required sections:
1. Partner Hero
2. Partner Field Visit Media
3. Value Pillars
4. Fundworks + Retention Narrative
5. Partner Process
6. Proof/Testimonials
7. Partner CTA

Minimum acceptance:
- Partner path is clearly differentiated from borrower path.
- Partner apply and direct call actions are visible and functional.

### Testimonials
Required sections:
1. Testimonials Hero
2. Featured Stories
3. Quote Grid
4. Final Conversion Prompt

Minimum acceptance:
- Proof content is dominant on page.
- Final CTA routes to canonical Apply path.

### Contact
Required sections:
1. Contact Hero (intent split messaging)
2. Direct Contact Cards
3. Contact Form
4. Social Links

Minimum acceptance:
- Contact form can capture intent category (`Funding`, `ISO`, `General`).
- Contact cards reflect verified phone/email details.

### Apply Entry
Required sections:
1. Apply Hero
2. What To Prepare checklist
3. Support Prompt

Minimum acceptance:
- Handoff to external apply endpoint functions correctly.
- Support contact is visible near conversion action.

### Company Principles (Light)
Required sections:
1. Principles Hero
2. Core Values
3. Commitment Statement

Minimum acceptance:
- Clear trust/ethics narrative.
- CTA to Contact or Apply present.

### Resources (Light Shell)
Required sections:
1. Resources Hero
2. Calculator Teaser (phase 2 coming soon)
3. Additional Resource Modules

Minimum acceptance:
- Clearly communicates educational intent and phase 2 tool roadmap.

## 4) QA Acceptance Checklist

| Category | Requirement | Pass/Fail | Notes |
|---|---|---|---|
| Navigation | Links render and route correctly | [ ] | |
| CTA Routing | All primary apply CTAs use canonical destination | [ ] | |
| Contact | Form submission path and direct cards work | [ ] | |
| Content | Section order matches approved wireframe flow | [ ] | |
| Mobile | CTA behavior and readability are acceptable | [ ] | |
| Compliance | Privacy/compliance links are present | [ ] | |

## 5) Dependencies Before Dev Complete
- Approved testimonial and logo asset set.
- Finalized video exports/captions for trust sections.
- Canonical apply URL and tracking convention.
- Verified contact details and response-time statement.

## 6) Handoff Bundle
Implementation should reference these files together:
- `docs/phase1-master-index.md`
- `docs/wireframe-phase1.md`
- `docs/wireframe-copy-placeholders-phase1.md`
- `docs/content-production-tracker-phase1.md`
- `docs/owner-assignment-sheet-phase1.md`
- `docs/phase1-launch-readiness-checklist.md`
- `docs/phase1-launch-day-runbook.md`
- `docs/phase1-decision-log.md`

## 7) Definition of Build Complete
- All required sections implemented per page.
- QA checklist passes with no critical failures.
- Go/no-go gates can be marked `Done` in launch-readiness checklist.
