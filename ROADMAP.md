# Roadmap

This roadmap is intentionally product- and safety-oriented. It is not a promise of dates.

## Now

### Identity resolution quality

- improve common-name collision tests
- expand username normalization
- improve broad-location comparison
- preserve source provenance through every transformation
- make weak identity evidence reduce confidence instead of creating more claims

### Search quality

- tune adaptive query generation
- reduce unnecessary provider calls
- improve duplicate-result handling
- improve source-type classification
- test freshness and stale-profile handling

### Result experience

- improve the identity-file experience on mobile
- make source confidence easier to understand
- show unresolved leads without implying they belong to the subject
- keep PASS / CHECK / FLAG tied to specific evidence rather than personality judgments

### Safety and privacy

- expand redaction tests
- expand youth/minor protections
- strengthen abuse-rate controls
- test correction/removal workflows
- document retention decisions before public reports launch

## Next

### Profile consistency

- stronger social-profile correlation
- account-history consistency signals
- username reuse/context checks
- source freshness indicators

### Contradiction detection

- identify material conflicts between corroborated public claims
- separate harmless stale data from meaningful contradictions
- require higher identity confidence for reputation-sensitive material

### Contributor tooling

- synthetic test fixture library
- provider mocks
- reproducible resolver benchmarks
- accessibility test checklist
- security review checklist

## Later

- limited public beta after launch-readiness gates are satisfied
- shareable result summaries that avoid exposing unnecessary personal data
- user-facing dispute/correction tracking
- stronger source freshness and provenance UI
- provider redundancy where legally and operationally appropriate

## Explicitly not on the roadmap

We are not trying to build:

- a home-address finder
- a live-location tracker
- a relatives-as-locators graph
- a government-ID or financial-data lookup tool
- a secret law-enforcement version
- a black-box "good person / bad person" score
- employment, housing, credit, insurance, admissions, licensing, or other regulated eligibility screening
- a system that treats an arrest, allegation, lawsuit, or same-name record as proof about the intended subject

## Launch principle

A search API key is not a launch decision.

Public reports stay gated until identity resolution, privacy, corrections, provider terms, abuse controls, security, legal/compliance review, and rollback procedures are ready together.
