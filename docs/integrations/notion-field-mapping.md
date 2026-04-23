# Notion Field Mapping (Lightweight)

This guide helps a buyer-side user or AI assistant map `hengcheng-garment-skill` vendor data into a Notion supplier database.

## Suggested Notion database properties
- Supplier Name (title)
- Supplier Type (select)
- Country (select/text)
- City (text)
- Capabilities (multi-select)
- Product Categories (multi-select)
- Working Languages (multi-select)
- Official Website (url)
- Contact Page (url)
- Inquiry Email (email)
- Status (select)
- Notes (text)

## Mapping table
| Skill field | Recommended Notion property |
|---|---|
| supplier_name | Supplier Name |
| supplier_type | Supplier Type |
| country | Country |
| city | City |
| capabilities | Capabilities |
| product_categories | Product Categories |
| working_languages | Working Languages |
| official_website | Official Website |
| preferred_contact_path | Contact Page |
| preferred_inquiry_email | Inquiry Email |

## Suggested usage
- Use the vendor record JSON as the source of truth
- Let a buyer-side AI assistant convert the JSON into Notion-ready property values
- Or use the flat CSV as a manual copy/import reference

## Notes
- This repository does **not** provide a Notion API client or OAuth flow.
- It is meant to reduce friction, not to become a full integration app.
