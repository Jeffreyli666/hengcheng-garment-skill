# Use Case: Inbound Inquiry Triage

This document explains how `hengcheng-garment-skill` can be used as a practical lead-filtering layer instead of a passive public knowledge base.

## Why this use case matters
Many inbound factory inquiries are under-specified, low-fit, price-only, or not serious enough for immediate human follow-up.
A useful AI workflow should help separate:
- likely-fit leads worth human attention
- possible-fit leads that need more information first
- weak-fit leads that should be declined or deprioritized politely

## Input sources
This skill can be used to evaluate inquiries from channels such as:
- website contact forms
- email inboxes
- LinkedIn messages
- sourcing-platform messages
- Fiverr / freelancer-style inbound leads
- internal spreadsheets or CRM rows

## Minimal workflow
1. Receive an inbound inquiry.
2. Extract key fields:
   - product category
   - quantity
   - target market
   - timeline
   - sample need
   - material / branding details
3. Compare the inquiry against the compiled rules in `compiled/hengcheng-master-context.md`.
4. Output standardized JSON using `schemas/evaluation-output.schema.json`.
5. Route the case by fit label.

## Suggested routing logic
### likely_fit
- human follow-up priority: high
- next step: request tech pack / sample details or move toward quotation discussion
- recommended pages: OEM / Private Label, Sample Development, Contact

### possible_fit
- human follow-up priority: medium
- next step: ask for missing core fields before committing time
- recommended pages: OEM / Private Label, Sample Development, FAQ

### weak_fit
- human follow-up priority: low
- next step: polite decline or low-priority holding reply
- avoid spending manual time unless the inquiry changes materially

## Example automation pattern
A basic workflow can look like this:
- trigger: new website form / new email / new platform message
- AI step 1: extract structured fields from the raw message
- AI step 2: evaluate fit using the Hengcheng rules
- AI step 3: produce JSON output + a short suggested reply
- router step:
  - likely_fit -> send to human / CRM hot lead queue
  - possible_fit -> send clarification reply template
  - weak_fit -> send polite low-fit reply or archive queue

## Why this is commercially useful
The value is not “AI for show”.
The value is:
- less time wasted on poor-fit inquiries
- faster first response to better-fit leads
- more consistent qualification logic
- more complete RFQs before human time is spent

## Important caution
This repository is a public rules / context layer, not a promise engine.
It should help triage and structure the inquiry, but it should not autonomously make unsupported claims about MOQ, price, compliance, or capacity.
