# Contributing

Thanks for taking an interest in Do They Pass.

This project deals with real people and public information, so contribution quality is not just about whether code works. A change can be technically correct and still be unsafe, misleading, invasive, or legally inappropriate.

## Good contributions

Useful contributions include:

- synthetic unit tests for identity collisions
- accessibility improvements
- mobile UX improvements
- source deduplication
- provider mocks
- URL and username normalization
- result-explanation clarity
- privacy redaction tests
- performance improvements
- documentation
- threat modeling
- abuse-prevention ideas
- OSINT methodology that preserves source provenance and uncertainty

## Before you propose a feature

Ask:

1. Does this help verify identity consistency?
2. Is the information necessary to answer that question?
3. Could this expose a precise private location or sensitive identifier?
4. Could a same-name collision harm the wrong person?
5. Would a reasonable user interpret the output as stronger than the evidence actually is?
6. Can the result preserve the source and uncertainty?

If the answer raises a privacy or safety concern, explain the concern in the proposal instead of silently working around it.

## Do not submit

Please do not submit code or feature proposals designed to:

- expose home addresses or live location
- reveal government identifiers, financial data, medical data, credentials, or private contact details
- locate minors or expose school/schedule information
- use relatives as a locator mechanism
- create stalking, harassment, blackmail, or doxxing features
- assign opaque character, guilt, danger, or trustworthiness scores
- enable regulated employment/housing/credit/etc. screening
- scrape sources in ways that clearly violate provider terms or access controls
- bypass authentication, paywalls, robots/access restrictions, or security controls

## Development approach

The production repository is private while the system is in early development. Public collaboration begins with specifications, synthetic fixtures, isolated components, UX, tests, documentation, and reviewed contributions that can later be integrated into the private application.

Never post production API keys, preview tokens, private search subjects, logs containing personal information, or private infrastructure details in a public issue or pull request.

## Issues

If you want to work on an issue, leave a short comment describing your approach before doing significant work. For larger changes, start with a design discussion rather than a large surprise pull request.

For security vulnerabilities, do not open a public issue. Use the security contact described at https://dotheypass.com/security.html.

## Pull requests

A good pull request should include:

- what changed
- why it matters
- how it was tested
- privacy/safety impact, if any
- screenshots for UI changes
- synthetic test cases for resolver or matching changes

## Tests

Identity-related work should use synthetic or clearly authorized test data. Do not add random real people as test fixtures.

## Conduct

Be constructive. Challenge ideas and implementation details without attacking contributors or search subjects. Personal information found during testing should not become discussion material unless it is strictly necessary, authorized, and handled through the private testing process.
