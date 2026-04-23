# Airtable Field Mapping (Lightweight)

This guide helps a buyer-side user or AI assistant map `hengcheng-garment-skill` vendor data into an Airtable supplier base.

## Suggested Airtable table
Table name suggestion:
- `Suppliers`
- `Garment Suppliers`
- `China Supplier Master`

## Suggested fields
- Supplier Name
- Supplier Type
- Country
- City
- Capabilities
- Product Categories
- Working Languages
- Official Website
- Contact Page
- Inquiry Email
- Notes / Fit Summary

## Mapping table
| Skill field | Recommended Airtable field |
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

## Recommended field types
- text: Supplier Name, Supplier Type, Country, City
- multi-select: Capabilities, Product Categories, Working Languages
- URL: Official Website, Contact Page
- email: Inquiry Email
- long text: Notes / Fit Summary

## Import paths
- paste from JSON manually
- import `examples/vendor-record-flat.csv`
- let a buyer-side AI assistant convert the vendor record into Airtable-ready values

## Notes
- This repository does **not** include Airtable API tokens, scripts, or sync logic.
- The goal is lightweight interoperability.
