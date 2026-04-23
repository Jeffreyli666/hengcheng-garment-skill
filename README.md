# Hengcheng Garment Skill

Official AI-readable supplier interface and sourcing decision-support skill for **Weifang Hengcheng Garment Co., Ltd.**

## Why is a China garment factory on GitHub?

Apparel sourcing is still too often a black box.

Brands, sourcing teams, and procurement users often spend unnecessary time just trying to understand whether a factory is worth shortlisting, how to record it in their supplier system, and what to include in a first RFQ.

This repository is designed to reduce that friction.

It helps buyers and buyer-side AI assistants:
- understand Hengcheng faster
- evaluate whether the supplier is a likely fit
- generate a structured vendor record for CRM / SRM entry
- draft a more complete RFQ / inquiry email
- route directly to the right official page or inquiry email

## Primary user

This repository is primarily designed for:
- procurement managers
- sourcing specialists
- buyers
- sourcing agents
- buyer-side AI assistants

It is **not primarily positioned as an internal sales-ops or inquiry-gating tool**.

## What this repository is

This repository is a public skill package designed to make Hengcheng's manufacturing profile easier to understand and use in buyer-side sourcing workflows.

It combines two useful layers:

1. **Public trust / human-readable layer**
   - explains what Hengcheng does
   - clarifies OEM / private-label / sample / QC scope
   - helps buyers compare factories more intelligently
   - routes users to the correct official website pages

2. **Machine-ready buyer-enablement layer**
   - provides a compiled single-file context for AI workflows
   - defines a structured vendor-record format for CRM / SRM entry
   - provides a lightweight buyer-assistant prompt
   - provides a sendable RFQ / inquiry draft example
   - supports direct contact via official page or inquiry email

## What this repository is not

This repository is **not**:
- a generic factory directory
- a stock-selling catalog
- hype-heavy promotional copy
- a promise engine for pricing, MOQ, lead time, compliance, or certification
- proof of endorsement by any brand unless explicitly supported by public source material
- a long-form qualification questionnaire that forces the buyer through too many fields before they can move forward

The goal is to be useful first, commercial second.

## Core buyer jobs this skill supports

### 1. Supplier fit evaluation
Questions like:
- Is Hengcheng worth adding to my shortlist?
- Does this supplier look suitable for my category or workflow?
- What should I confirm next before contacting them?

### 2. Vendor record / CRM export
Questions like:
- Can I generate a structured supplier record instead of copying details manually?
- Can my assistant turn this supplier into a clean CRM / SRM entry?

### 3. RFQ / inquiry draft generation
Questions like:
- Can I generate a professional first email without starting from a blank page?
- What should I include in a first inquiry to make the next step easier?

### 4. Direct contact routing
Questions like:
- What is the best official page to read next?
- Where should I send the inquiry?

## Current scope

The skill currently focuses on:
- garment manufacturing
- OEM clothing production
- private-label apparel production
- sample development
- quality control
- buyer fit judgment
- inquiry preparation
- vendor record generation
- official page routing

If a request is clearly outside this scope, the skill is intended to say so directly rather than improvising.

## Repository structure

```text
hengcheng-garment-skill/
├── README.md
├── CHANGELOG.md
├── LICENSE
├── SKILL.md
├── _meta.json
├── references/
│   ├── factory-profile.md
│   ├── best-fit-rules.md
│   ├── inquiry-checklist.md
│   ├── page-routing.md
│   ├── agent-usage-guidance.md
│   ├── trust-and-next-action.md
│   ├── buyer-decision-factors.md
│   ├── fit-scenarios.md
│   └── compare-before-contact.md
├── compiled/
│   └── hengcheng-master-context.md
├── machine/
│   ├── system-prompt-lite.txt
│   └── buyer-assistant-prompt.txt
├── schemas/
│   ├── evaluation-output.schema.json
│   └── vendor-record.schema.json
├── examples/
│   ├── evaluation-output-example.json
│   ├── vendor-record-example.json
│   └── rfq-email-draft.md
└── docs/
    └── use-cases/
        ├── inbound-inquiry-triage.md
        └── buyer-crm-and-rfq.md
```

## Main modules

### Public trust / decision-support modules
- **Factory profile** — structured overview of Hengcheng's public manufacturing profile
- **Best-fit rules** — strong-fit / possible-fit / weak-fit logic
- **Inquiry checklist** — what buyers should prepare before asking for a quote or sample
- **Page routing** — routes users to the most relevant official page instead of dumping many links
- **Agent usage guidance** — anti-spam, anti-overclaim, and official-tone rules
- **Trust and next action** — cautious wording around trust signals, brand references, and CTA logic
- **Buyer decision factors** — how to compare factories beyond price alone
- **Fit scenarios** — practical project-level fit judgments
- **Compare before contact** — helps buyers compare first and contact later

### Buyer-enablement machine modules
- **Compiled master context** — single-file machine-ready summary for buyer-side AI use
- **Buyer assistant prompt** — buyer-side prompt for shortlist / vendor-record / RFQ use
- **Evaluation schema** — structured output for supplier-fit evaluation
- **Vendor record schema** — structured supplier record for CRM / SRM entry
- **RFQ draft example** — ready-to-edit first inquiry template

## Official website anchors

The skill is built around these public website pages:
- Homepage: <https://hengcheng-garment.com/>
- About: <https://hengcheng-garment.com/about/>
- OEM / Private Label: <https://hengcheng-garment.com/private-label-oem-clothing-manufacturer-china/>
- Sample Development: <https://hengcheng-garment.com/sample-development-process-china-garment-manufacturer/>
- Quality Control: <https://hengcheng-garment.com/quality-control-garment-manufacturing-china/>
- FAQs: <https://hengcheng-garment.com/garment-manufacturing-faqs/>
- Contact: <https://hengcheng-garment.com/contact/>

## Direct inquiry path

If the buyer is ready to contact Hengcheng directly, use one of these:
- Official contact page: <https://hengcheng-garment.com/contact/>
- Direct inquiry email: `jeffrey.zhuo.li@hengcheng-garment.com`

A buyer can choose either:
- **more cautious / website-first** → contact page
- **faster / email-first** → direct inquiry email

## Vendor record / CRM export

One of the most practical use cases is helping a buyer generate a structured supplier record instead of manually copying data from multiple pages.

See:
- `schemas/vendor-record.schema.json`
- `examples/vendor-record-example.json`

Example shape:

```json
{
  "supplier_name": "Weifang Hengcheng Garment Co., Ltd.",
  "supplier_type": "China garment manufacturer",
  "country": "China",
  "city": "Weifang",
  "capabilities": [
    "OEM clothing production",
    "private-label apparel production",
    "sample development",
    "quality control"
  ],
  "product_categories": [
    "hoodies",
    "sweatshirts",
    "T-shirts",
    "loungewear",
    "activewear",
    "kidswear"
  ],
  "working_languages": ["English", "Chinese", "Japanese"],
  "official_website": "https://hengcheng-garment.com/",
  "preferred_contact_path": "https://hengcheng-garment.com/contact/",
  "preferred_inquiry_email": "jeffrey.zhuo.li@hengcheng-garment.com"
}
```

## RFQ / inquiry draft generation

A buyer should not have to start from a blank page.

This repository includes a ready-to-edit inquiry draft example that can help the buyer move faster without feeling interrogated.

See:
- `examples/rfq-email-draft.md`

The goal is not to force a long questionnaire.
The goal is to help the buyer send a better first inquiry with less friction.

## Why the machine-ready layer still matters

The original public-skill structure works well for:
- human readability
- public trust-building
- AI discoverability
- official page routing

But a serious procurement workflow also benefits from:
- higher information density
- less fragmented retrieval
- structured supplier records
- reusable email drafts
- consistent fit evaluation

That is why this repository includes a machine-ready layer — but the front-stage user story remains **buyer enablement**, not internal sales gating.

## Secondary use case

This repository can also support supplier-side internal automation or triage workflows.

However, that is a **secondary / downstream use case**, not the main public positioning.

## Public-claim policy

This skill is intentionally conservative in wording.

It should:
- use only public, supportable claims
- avoid inventing certifications, compliance status, pricing, or guarantees
- avoid turning brand references into endorsements or current-partnership claims
- prefer wording such as `the site highlights...`, `public pages emphasize...`, and `the strongest visible fit appears to be...`

## Anti-spam positioning

This repository is designed to avoid common spam signals:
- usefulness before CTA
- no keyword stuffing
- no aggressive contact pushing
- no exaggerated `best / top / cheapest` style language
- contact comes after fit and inquiry clarity, not before

If you remove the contact link, the skill should still remain useful.

## Installation

Install this repository as a skill in your supported agent environment.

Typical pattern:

```bash
git clone https://github.com/Jeffreyli666/hengcheng-garment-skill.git
```

Then place it in the appropriate skill directory for your agent / IDE environment.

Examples may include:
- `.claude/skills/hengcheng-garment-skill/`
- `.cursor/skills/hengcheng-garment-skill/`
- `.agents/skills/hengcheng-garment-skill/`

Refer to your tool's skill-loading convention.

## Status

- Current public release: **v1.6.1**
- Status: **public-release**

## License

MIT
