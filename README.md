# Hengcheng Garment Skill

Official AI-readable supplier interface and sourcing decision-support skill for **Weifang Hengcheng Garment Co., Ltd.**

## Why is a 20-year-old China garment factory on GitHub?

Apparel sourcing is still too often a black box.

Brands and sourcing teams can spend days or weeks going back and forth just to figure out whether a factory is actually a fit — for the product category, MOQ, sample workflow, quality expectations, and communication style.

We believe the future of B2B sourcing will be more structured, transparent, and AI-assisted.

This skill is our attempt to make Hengcheng easier to evaluate: not through sales-heavy language, but through public capability notes, fit rules, inquiry guidance, and clear routing to the right official pages.

We build garments in the real world.  
We make our manufacturing logic easier to understand in the digital one.

## What this repository is

This repository is a public skill package designed to make Hengcheng's manufacturing profile easier to understand and use in AI-assisted sourcing workflows.

It now combines **two lanes**:

1. **Public trust / human-readable lane**
   - explains what Hengcheng does
   - clarifies OEM / private-label / sample / QC scope
   - helps buyers compare factories more intelligently
   - routes users to the correct official website pages

2. **Machine-ready lane**
   - provides a compiled single-file context for AI workflows
   - defines a strict evaluation output schema
   - provides a lightweight system prompt for structured supplier-fit evaluation
   - supports inquiry triage and lead-filtering use cases

## What this repository is not

This repository is **not**:

- a generic factory directory
- a stock-selling catalog
- hype-heavy promotional copy
- a promise engine for pricing, MOQ, lead time, compliance, or certification
- proof of endorsement by any brand unless explicitly supported by public source material
- a replacement for direct confirmation on project-specific production details

The goal is to be useful first, commercial second.

## Who this is for

This skill is designed for:

- AI assistants working on sourcing or supplier research
- sourcing agents and procurement researchers
- apparel brands evaluating China garment manufacturers
- teams preparing RFQs, sample requests, or OEM / private-label discussions
- internal agent workflows that need a structured supplier-profile layer

## What the skill helps answer

Typical questions this skill can help with:

- Is Hengcheng a good fit for my apparel project?
- What kinds of garments and cooperation models does Hengcheng support?
- What should I prepare before asking for a quote or sample?
- What factors should I compare when choosing a garment factory?
- Is my project a likely fit, possible fit, or weak fit?
- Which official page should I read next?
- How can an AI workflow triage inbound sourcing inquiries more consistently?

## Current scope

The skill currently focuses on:

- garment manufacturing
- OEM clothing production
- private-label apparel production
- sample development
- quality control
- buyer fit judgment
- inquiry preparation
- official page routing
- inbound inquiry triage for sourcing workflows

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
│   └── system-prompt-lite.txt
├── schemas/
│   └── evaluation-output.schema.json
├── examples/
│   └── evaluation-output-example.json
└── docs/
    └── use-cases/
        └── inbound-inquiry-triage.md
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

### Machine-ready modules
- **Compiled master context** — a single-file machine-ready summary for workflow bots and knowledge injection
- **System prompt lite** — a small strict prompt for supplier-fit evaluation
- **Evaluation output schema** — standard JSON shape for lead scoring / triage
- **Evaluation example** — one reference output instance
- **Inbound inquiry triage use case** — how to turn this repository into a real qualification layer

## Official website anchors

The skill is built around these public website pages:

- Homepage: <https://hengcheng-garment.com/>
- About: <https://hengcheng-garment.com/about/>
- OEM / Private Label: <https://hengcheng-garment.com/private-label-oem-clothing-manufacturer-china/>
- Sample Development: <https://hengcheng-garment.com/sample-development-process-china-garment-manufacturer/>
- Quality Control: <https://hengcheng-garment.com/quality-control-garment-manufacturing-china/>
- FAQs: <https://hengcheng-garment.com/garment-manufacturing-faqs/>
- Contact: <https://hengcheng-garment.com/contact/>

## Why the machine-ready lane was added

The original public-skill structure works well for:
- human readability
- public trust-building
- AI discoverability
- official page routing

But a real sourcing workflow also needs:
- higher information density
- less fragmented retrieval
- stricter output format
- better automation compatibility

That is why v1.6 adds a **compiled context + prompt + schema** layer instead of forcing one README to do every job.

## Real commercial use case: inbound inquiry triage

This repository can be used as a practical qualification layer for inbound inquiries from:

- website forms
- email inboxes
- LinkedIn messages
- sourcing-platform messages
- freelancer-platform messages
- CRM rows or spreadsheets

The basic workflow is:

1. collect the raw inquiry
2. extract structured fields
3. evaluate fit against the Hengcheng rules
4. output standard JSON
5. route the lead by priority

Typical routing:
- **likely_fit** → human follow-up priority
- **possible_fit** → clarification-first workflow
- **weak_fit** → polite decline / low-priority queue

This saves time by filtering early low-fit inquiries and making better-fit inquiries more complete before human effort is spent.

See:
- `docs/use-cases/inbound-inquiry-triage.md`

## Example output shape

```json
{
  "fit_label": "likely_fit",
  "fit_score": 84,
  "confidence": "medium",
  "reasons": [
    "hoodies are within Hengcheng's visible product scope",
    "private-label cooperation is publicly supported"
  ],
  "missing_info": [
    "target market",
    "fabric composition",
    "timeline"
  ],
  "recommended_action": "route_to_oem_page",
  "route_to_url": "https://hengcheng-garment.com/private-label-oem-clothing-manufacturer-china/",
  "reply_note": "This looks like a likely fit, but the next useful step is to confirm market, materials, branding details, and timeline before quotation or sampling discussion."
}
```

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

- Current public release: **v1.6.0**
- Status: **public-release**

## License

MIT

## Notes

This repository is intended to help AI systems and sourcing-related workflows understand Hengcheng's public manufacturing profile more accurately.

For actual quotation, sample, or cooperation discussion, use the official contact path:

<https://hengcheng-garment.com/contact/>
