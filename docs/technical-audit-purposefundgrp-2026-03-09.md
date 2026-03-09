# Technical Audit - purposefundgrp.com

Date: 2026-03-09  
Audit type: External black-box audit (URL-only, no backend/CMS access)  
Primary URL: https://purposefundgrp.com/

## Executive Summary
The site is online, HTTPS is enforced, and core public routes respond correctly. The biggest technical risks are incomplete security hardening headers, missing favicon delivery, and weak technical SEO structure (canonical not detected, shallow robots directives, and heading hierarchy quality).

## Findings (Ordered by Severity)

### High
1. Missing key HTTP security headers
- Observed on `https://purposefundgrp.com/` response headers:
  - Present: `Strict-Transport-Security`, `Content-Security-Policy`
  - Missing: `X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy`, `Permissions-Policy`
- Impact:
  - Clickjacking risk surface is higher without explicit frame policy.
  - MIME sniffing protections are weaker without `X-Content-Type-Options`.
  - Privacy and browser capability constraints are less controlled.
- Recommendation:
  - Add missing headers at CDN/hosting layer (GoDaddy site config or edge proxy).

2. Missing favicon endpoint
- `https://purposefundgrp.com/favicon.ico` returns `404`.
- Impact:
  - Browser tab/icon rendering degrades and can reduce trust polish.
- Recommendation:
  - Publish favicon assets (`.ico`, plus modern PNG variants) and ensure root-level delivery.

### Medium
1. Technical SEO: canonical link not detected on homepage
- Homepage includes title, meta description, and OG tags.
- A canonical tag was not detected in the homepage HTML snapshot.
- Impact:
  - Potential duplicate URL ambiguity for search engines.
- Recommendation:
  - Add `<link rel="canonical" href="https://purposefundgrp.com/">`.

2. Heading hierarchy quality can be improved
- Detected heading counts on homepage:
  - `h1`: 1
  - `h2`: 0
  - `h3`: 0
  - `h4`: 13
- Impact:
  - Reduced semantic clarity for accessibility and SEO context.
- Recommendation:
  - Rework section headings so major sections use `h2`, subsections use `h3`.

3. Robots and sitemap configuration is minimal
- `robots.txt` content observed: `User-agent: *` and `Disallow: /404%`
- `sitemap.xml` present and references child sitemaps.
- Impact:
  - Crawl directives are very sparse; sitemap is not explicitly referenced in robots.
- Recommendation:
  - Add explicit sitemap line and a clearer robots policy.

4. Short cache max-age on HTML
- `Cache-Control: max-age=30` on homepage response.
- Impact:
  - More frequent origin hits and lower cache efficiency.
- Recommendation:
  - Keep short cache for HTML only if needed; increase static asset cache TTLs aggressively.

### Low
1. Route naming consistency is mixed
- Working routes include:
  - `/contact-us`
  - `/iso-partnership`
  - `/socials-%26-testimonials`
  - `/privacy-policy-1`
- Impact:
  - Inconsistent slug style can reduce clarity and maintainability.
- Recommendation:
  - Standardize slugs over time (with 301s), e.g. hyphenated, clean semantic paths.

2. Analytics fingerprint not clearly detected in homepage HTML snapshot
- Common tracker markers were not detected in static HTML pass.
- Impact:
  - Could indicate no analytics, deferred script injection, or bundled/minified loading path.
- Recommendation:
  - Verify analytics events using browser devtools network/runtime on key conversion actions.

## Evidence Snapshot

### Protocol and transport
- `http://purposefundgrp.com` -> `301` redirect to HTTPS.
- `https://purposefundgrp.com/` -> `200`.

### Header highlights
- Present:
  - `Strict-Transport-Security: max-age=63072000; includeSubDomains; preload`
  - `Content-Security-Policy: frame-ancestors ...`
- Missing:
  - `X-Frame-Options`
  - `X-Content-Type-Options`
  - `Referrer-Policy`
  - `Permissions-Policy`

### Timing snapshot (single sample)
- `time_starttransfer`: ~0.615s
- `time_total`: ~0.663s
- `size_download`: ~110047 bytes

### Endpoint health
- `GET /` -> `200`
- `GET /contact-us` -> `200`
- `GET /iso-partnership` -> `200`
- `GET /socials-%26-testimonials` -> `200`
- `GET /privacy-policy-1` -> `200`
- `GET /robots.txt` -> `200`
- `GET /sitemap.xml` -> `200`
- `GET /favicon.ico` -> `404`

## Priority Remediation Plan
1. Add missing security headers at edge/hosting layer.
2. Publish favicon assets and verify `/favicon.ico` returns `200`.
3. Add canonical tag on homepage and validate via page source.
4. Improve heading hierarchy (`h2`/`h3`) across major sections.
5. Expand robots directives and include explicit sitemap location.
6. Run browser-based Core Web Vitals + Lighthouse pass for mobile/desktop and attach scorecard.

## Scope Notes
This audit is URL-only and external. It does not include:
- CMS/template internals,
- server logs,
- conversion event QA in browser runtime,
- authenticated/private workflows,
- JavaScript runtime error trace.

A deeper phase can add Lighthouse, accessibility scanning (axe), and full crawl-based broken link/image checks.
