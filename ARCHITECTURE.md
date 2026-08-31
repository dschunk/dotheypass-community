# Architecture Overview

This document describes the conceptual pipeline without exposing production secrets or private infrastructure details.

## High-level flow

1. **Intake**
   - name
   - optional broad location
   - optional username
   - optional public profile URL

2. **Normalization**
   - trim and normalize input
   - normalize username forms
   - validate public profile URLs
   - avoid turning the input into invasive locator queries

3. **Search providers**
   - retrieve candidate public-web results
   - keep provider credentials server-side
   - use an adaptive query budget instead of blindly spending maximum queries

4. **Identity resolution**
   Candidate results are not automatically treated as the intended person.

   Evidence can be classified as:
   - `CONFIRMED`
   - `LIKELY_MATCH`
   - `POSSIBLE_MATCH`
   - `UNCONFIRMED`
   - `SUPPRESSED`

   Name-only evidence is intentionally weak. Additional corroborating signals such as username, broad location, or an exact submitted public profile are needed before confidence increases.

5. **Policy / privacy filtering**
   Before evidence can be displayed, filters can suppress or redact material that should not be surfaced, including categories such as:
   - sensitive identifiers
   - precise private addresses
   - contact data
   - precise coordinates
   - youth/minor locator information
   - weakly matched reputation-sensitive material

6. **Evidence model**
   Every meaningful finding should preserve:
   - source URL
   - source type
   - observed signal
   - match confidence
   - reason for the classification
   - freshness/context where available

7. **Report model**
   Consumer-facing statuses are intentionally simpler than internal evidence states:
   - `PASS`
   - `CHECK`
   - `FLAG`
   - `PENDING`
   - `UNAVAILABLE`

   These describe the checked evidence. They are not a character score or safety guarantee.

8. **Corrections and removals**
   A production system must have a practical way for a subject to challenge a wrong match or information the product controls.

9. **Abuse controls**
   - request limits
   - protected engineering endpoints
   - launch flags
   - noindex/no-store handling for private result surfaces
   - input limits
   - security headers

## Current provider approach

The protected engineering preview is Tavily-first with an optional Brave fallback. Provider choice is an implementation detail; the resolver and privacy layer should not depend on one provider's response format.

## Important engineering principle

**Search retrieval and identity attribution are separate problems.**

A search engine returning a page for a name does not prove that page belongs to the intended person. The resolver must earn attribution from corroborating signals.

## Public vs private code

The production application is currently private while the system is early and launch-sensitive. This public community space is intended for discussion, specifications, isolated components, tests, fixtures, UX work, and reviewed contributions that do not expose secrets or real private search data.
