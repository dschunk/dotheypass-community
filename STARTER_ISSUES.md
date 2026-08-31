# Starter Issue Backlog

These are candidate issues for the public community repository. They are intentionally scoped so contributors can help without access to production secrets or private search data.

## 1. Build synthetic common-name collision fixtures

**Area:** testing / identity resolution

Create a reusable set of synthetic people who share names but differ in location, username, employer, profile URL, or chronology.

**Goal:** make it easy to test that a resolver does not merge two people simply because their names match.

**Deliverables:**
- JSON or JS fixtures
- expected CONFIRMED / LIKELY / POSSIBLE / UNCONFIRMED outcomes
- edge-case notes

---

## 2. Username normalization test suite

**Area:** engineering

Design tests for equivalent username forms such as `@alex`, `alex`, profile URLs, case differences, trailing slashes, and common platform URL variants.

**Goal:** normalize useful variants without creating false identity matches.

---

## 3. Source URL canonicalization and deduplication

**Area:** engineering / search

Define a safe canonicalization strategy for duplicate search results that differ only by tracking parameters, fragments, mobile subdomains, or harmless URL formatting.

**Goal:** avoid counting the same public source multiple times as corroboration.

---

## 4. Mobile identity-file UX review

**Area:** design / frontend

Review the public identity-file concept on narrow mobile screens and propose improvements for hierarchy, source readability, status explanation, and unresolved leads.

**Deliverables:**
- screenshots or wireframes
- accessibility considerations
- CSS/HTML prototype welcome

---

## 5. Accessibility audit checklist

**Area:** accessibility / frontend

Create a practical checklist for the search page, forms, identity file, trust pages, and status labels.

Include keyboard navigation, focus treatment, screen reader labeling, color contrast, touch targets, zoom/text scaling, and reduced-motion expectations.

---

## 6. Public-source freshness model

**Area:** search / research

Propose a simple way to represent source freshness without pretending every page has a reliable publication date.

Questions:
- how should explicit dates differ from inferred/stale indicators?
- when should an old profile reduce confidence?
- how should the UI communicate unknown freshness?

---

## 7. Provider mock interface

**Area:** engineering / testing

Design a provider-neutral mock response format that can simulate Tavily, Brave, or another search provider without network calls.

**Goal:** identity-resolution tests should not depend on live search APIs.

---

## 8. Contradiction taxonomy

**Area:** trust & safety / OSINT / product

Define what should count as a meaningful contradiction versus harmless stale or incomplete data.

Examples to consider:
- broad location changes over time
- job-title changes
- usernames that changed
- duplicate profiles
- conflicting current-city claims

**Important:** the taxonomy must preserve uncertainty and avoid turning ordinary life changes into a FLAG.

---

## 9. Privacy redaction fixture library

**Area:** privacy / testing

Create synthetic snippets containing emails, phone numbers, street addresses, coordinates, IDs, and mixed benign text.

**Goal:** verify that sensitive patterns are redacted without destroying useful identity context.

---

## 10. Threat model for public identity checks

**Area:** security / trust & safety

Document realistic abuse cases and mitigations.

Consider:
- stalking
- harassment
- automated bulk lookup
- targeted doxxing
- scraping result pages
- token leakage
- provider-key exposure
- malicious correction requests
- false-match amplification

Prioritize risks by likelihood and impact, and propose controls that do not require invasive user surveillance.

---

## 11. Loading-state UX for adaptive search

**Area:** frontend / product

Design a loading experience where each visible stage corresponds to real backend work rather than fake progress.

Possible stages:
- searching public sources
- matching identity signals
- resolving duplicates
- applying privacy rules
- preparing the file

---

## 12. Source-confidence explanation copy

**Area:** UX writing / trust & safety

Write short, plain-language explanations for:
- CONFIRMED
- LIKELY MATCH
- POSSIBLE MATCH
- UNCONFIRMED
- SUPPRESSED / not displayed

The wording should be understandable to a nontechnical user and should not overstate what the system knows.
