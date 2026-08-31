# Safety and Privacy Principles

Do They Pass works with public information about real people. That creates an obligation to minimize harm, not just maximize retrieval.

## Core rules

### Public does not automatically mean appropriate to surface

A piece of information being technically accessible on the internet is not, by itself, a reason to display it in a consolidated identity report.

### Identity confidence comes before negative claims

Potentially harmful or reputation-sensitive material requires stronger identity matching than ordinary profile information. Weak matches should be suppressed or left unresolved.

### Unknown is not false

If the system cannot establish a fact, the output should remain unknown or unresolved rather than converting uncertainty into a negative conclusion.

### Same name is not same person

Common-name collisions are a first-class safety problem. Name-only search results must not be treated as confirmed identity evidence.

### Minimize locator data

The product should not become a tool for finding precise home addresses, live locations, school schedules, relatives, or other data that materially increases offline locating risk.

### Extra protection for minors

Minor-related results should be narrower and focused on account authenticity/consistency rather than broad personal dossiers. Precise locator information should be suppressed.

## Data categories we do not want surfaced

- government identification numbers
- financial account information
- medical information
- passwords or credentials
- precise private home addresses
- live location
- precise coordinates
- private contact details used as locator vectors
- relatives/family members used to locate a subject
- youth school/schedule/location details

## Reputation-sensitive information

Material involving allegations, arrests, criminal records, lawsuits, accusations, or similarly sensitive claims needs strong identity matching, credible provenance, relevant context, and a correction path before it can ever be considered for consumer display.

A result merely appearing in search is not enough.

## No character scoring

Do They Pass should not output opaque labels such as:

- safe / unsafe person
- good / bad person
- trustworthy / untrustworthy person
- liar
- criminal
- dangerous

PASS / CHECK / FLAG describe the consistency of checked signals, not the worth or character of a human being.

## Prohibited product direction

Contributions that materially improve stalking, harassment, doxxing, intimidation, discrimination, blackmail, or regulated background-screening use should not be accepted.

## Corrections matter

False identity attribution is a safety incident. A production system needs a real path to correct or remove product-controlled information and to investigate mismatches.

## Testing

Use synthetic fixtures by default. Real-person testing should be limited to authorized/self-testing situations and should never result in public issue threads containing unnecessary personal information.
