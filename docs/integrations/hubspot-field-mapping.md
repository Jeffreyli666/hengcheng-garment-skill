# HubSpot Field Mapping (Lightweight)

This guide helps a buyer-side user or AI assistant map `hengcheng-garment-skill` vendor data into a HubSpot-style company / supplier record.

## Goal
Use the skill's structured vendor record to avoid manually copying supplier information into HubSpot.

## Recommended minimal HubSpot properties
Use standard or custom properties such as:
- Company Name
- Website
- Country/Region
- City
- Supplier Type (custom)
- Product Categories (custom multi-select)
- Capabilities (custom multi-select)
- Working Languages (custom multi-select)
- Preferred Contact Path (custom text/url)
- Preferred Inquiry Email (custom email/text)

## Mapping table
| Skill field | Recommended HubSpot property |
|---|---|
| supplier_name | Company Name |
| official_website | Website |
| country | Country/Region |
| city | City |
| supplier_type | Supplier Type |
| product_categories | Product Categories |
| capabilities | Capabilities |
| working_languages | Working Languages |
| preferred_contact_path | Preferred Contact Path |
| preferred_inquiry_email | Preferred Inquiry Email |

## Practical import paths
### Option 1: Manual copy
- Generate the vendor record JSON
- Paste values into HubSpot company properties

### Option 2: CSV import
- Use `examples/vendor-record-flat.csv`
- Rename columns to your internal HubSpot property names if needed
- Import as a company/supplier row

### Option 3: Buyer-side AI assistant
- Ask your assistant to transform the vendor record into your HubSpot import format
- Then paste/import the transformed row

## Notes
- This repository does **not** provide direct HubSpot API integration.
- The purpose is lightweight buyer enablement, not heavy SaaS integration.
