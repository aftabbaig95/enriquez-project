# Phase 1 KPI Dictionary

Project: Enriquez Project  
Version: v1  
Date: 2026-03-07  
Purpose: Define KPI formulas, data sources, and interpretation rules for consistent reporting.

## 1) Conversion KPI Definitions

| KPI ID | KPI Name | Formula | Data Source | Interpretation |
|---|---|---|---|---|
| K-001 | Application starts | Count of apply sessions initiated in period | Apply endpoint logs | Higher indicates stronger conversion intent |
| K-002 | Apply CTA click-through rate | Apply CTA clicks / page sessions | Tracking-tagged click events | Measures CTA effectiveness |
| K-003 | Contact form submissions | Count of successful form submissions | Contact form pipeline | Measures inquiry capture effectiveness |
| K-004 | ISO inquiry starts | ISO CTA clicks or ISO form starts | ISO path tracking events | Measures partner-path conversion activity |

## 2) Engagement KPI Definitions

| KPI ID | KPI Name | Formula | Data Source | Interpretation |
|---|---|---|---|---|
| K-101 | Home scroll completion | Sessions reaching target depth / Home sessions | Scroll depth events | Indicates content consumption quality |
| K-102 | Time on key pages | Average engaged time across Home/ISO/Testimonials | Session analytics | Indicates depth of evaluation |
| K-103 | FAQ engagement rate | FAQ interactions / page sessions containing FAQ | FAQ interaction events | Indicates objection-handling utilization |
| K-104 | Testimonial engagement rate | Testimonial interactions / testimonial page sessions | Video/quote interaction events | Indicates trust-proof engagement |

## 3) Operational KPI Definitions

| KPI ID | KPI Name | Formula | Data Source | Interpretation |
|---|---|---|---|---|
| K-201 | Median first-response time | Median(response timestamp - inquiry timestamp) | Follow-up logs/CRM | Lower is better |
| K-202 | Lead routing accuracy | Correctly routed leads / total leads | Routing audit sample or system logs | Higher indicates operational quality |
| K-203 | Unanswered inquiry rate | Inquiries with no response / total inquiries | Follow-up logs | Lower is better |

## 4) Data Hygiene Rules
- Use one canonical apply URL and standardized tracking tags.
- Ensure contact form captures intent category.
- Define period start/end consistently for every weekly report.
- Document anomalies (tracking outages, partial data).

## 5) Reporting Interpretation Bands
- Green: on or above target trajectory.
- Yellow: within manageable variance, mitigation required.
- Red: materially off trajectory, corrective plan required.

## 6) Related Docs
- `docs/phase1-kpi-baseline-and-targets.md`
- `docs/phase1-kpi-weekly-report-template.md`
- `docs/phase1-weekly-execution-dashboard.md`
