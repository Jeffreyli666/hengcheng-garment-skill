# Use Case: Buyer CRM Entry and RFQ Enablement

This repository is primarily designed for buyer-side procurement workflows, not only for supplier-side internal operations.

## Primary user
- procurement manager
- sourcing specialist
- sourcing agent
- buyer-side AI assistant

## Core buyer jobs
1. decide whether Hengcheng is worth adding to a shortlist
2. generate a structured vendor record instead of manually copying supplier information
3. generate a professional RFQ / inquiry draft with less friction
4. route to the official contact page or direct inquiry email

## Practical output types
### 1. Supplier-fit summary
Used when the buyer asks:
- is this supplier likely to fit my project?
- what should I confirm next?

### 2. Vendor record / CRM export
Used when the buyer wants to add Hengcheng to:
- CRM
- SRM
- supplier master
- sourcing spreadsheet
- internal procurement notes

Recommended files:
- `schemas/vendor-record.schema.json`
- `examples/vendor-record-example.json`

### 3. RFQ / inquiry draft
Used when the buyer wants a sendable first message without starting from a blank page.

Recommended file:
- `examples/rfq-email-draft.md`

### 4. One-click contact action
Use one of these:
- official contact page: https://hengcheng-garment.com/contact/
- direct inquiry email: jeffrey.zhuo.li@hengcheng-garment.com
- one-click mailto template: `examples/rfq-email-mailto.md`

## Why this is buyer-friendly
A buyer usually wants to move faster, not fill in a long form.
So the best front-stage experience is:
- help them understand the supplier quickly
- help them record the supplier quickly
- help them draft an inquiry quickly
- then give a direct contact path

## Secondary / non-primary use case
This repository can also support supplier-side internal triage or automation workflows, but that is not the main public user story and should not dominate the repository positioning.
