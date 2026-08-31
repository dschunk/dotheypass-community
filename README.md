# Do They Pass? — Community

**Look them up before you meet up.**

This repository is the public contributor and engineering community space for [Do They Pass?](https://dotheypass.com), an early-stage public-information identity consistency product.

The production application and private infrastructure are maintained separately. This community repository exists so engineers, researchers, designers, testers, security people, and trust & safety contributors can understand the problem, discuss approaches, and work on clearly scoped tasks without exposing production secrets or private systems.

## What is Do They Pass?

The core question is simple:

> Does the public story behind an online identity actually line up?

A user may know a name, broad location, username, or public profile. The product is being designed to review relevant public signals while preserving uncertainty and avoiding the common failure mode of attaching every same-name result to the same person.

The product is **not** intended to decide whether someone is a good person, safe, guilty, trustworthy, employable, creditworthy, or otherwise eligible for regulated decisions.

## Current status

The public product shell is live at **https://dotheypass.com**.

Current engineering includes:

- Cloudflare Workers
- Vanilla HTML / CSS / JavaScript
- Tavily-backed public-web search in a protected engineering preview
- conservative identity resolution
- CONFIRMED / LIKELY / POSSIBLE / UNCONFIRMED evidence states
- source provenance
- privacy redaction and suppression
- same-name collision handling
- rate limiting and abuse controls
- automated regression and safety tests

Unrestricted public identity reports are **not enabled yet**. Accuracy, privacy, safety, correction mechanisms, and legal review are launch gates rather than cleanup work after launch.

## Where help is useful

We are especially interested in contributors with experience or curiosity around:

- JavaScript / TypeScript
- Cloudflare Workers
- search APIs and information retrieval
- entity / identity resolution
- OSINT methodology
- frontend and mobile UX
- security engineering
- privacy engineering
- abuse prevention
- trust & safety
- automated testing
- accessibility

You do not need to know all of these areas.

## Start here

1. Read [CONTRIBUTING.md](CONTRIBUTING.md).
2. Read [ARCHITECTURE.md](ARCHITECTURE.md) for the conceptual pipeline.
3. Read [SAFETY.md](SAFETY.md) before proposing features involving personal data.
4. Review [ROADMAP.md](ROADMAP.md).
5. Pick a starter issue or suggest an improvement.

## Important boundaries

Do They Pass is for personal identity consistency checks involving public information. It is not a consumer reporting agency and is not for employment, housing, credit, insurance, lending, admissions, licensing, government benefits, or other regulated eligibility decisions.

We do not want contributions that make the product better at stalking, doxxing, exposing precise private locations, surfacing sensitive identifiers, or assigning opaque character/safety scores to people.

## Interested in contributing?

Visit **https://dotheypass.com/join.html** or participate through the issues in this repository.

This is currently an **early collaborator / volunteer project, not a job posting**.
