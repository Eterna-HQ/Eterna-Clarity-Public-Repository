# Open Household Records Taxonomy

**Version:** 0.1.0  
**Status:** Public review candidate  
**Namespace:** `ohrt`  
**Maintainer:** Eterna Clarity

The Open Household Records Taxonomy (OHRT) is a practical, software-independent way to classify the records that accumulate around everyday household life.

Its core rule is simple:

> Give each record one primary home based on what it is mainly about. Keep its other connections as relationships, tags, or references rather than creating competing copies.

The taxonomy is designed to work across paper folders, cloud storage, spreadsheets, software products, migration tools, and AI-assisted systems. A product may present fewer or broader categories while mapping them to this reference model.

## Start with the retrieval question

When a record could fit in several places, ask:

**If this record disappeared, which part of household life would notice first?**

That usually produces a better primary category than the file format, the organization that issued it, or the reason it happened to arrive today.

Examples:

| Record | Primary family | Useful relationships |
| --- | --- | --- |
| Home insurance policy | Insurance | Home & property |
| Vehicle repair invoice | Vehicles & transportation | Household assets, receipts & warranties; financial |
| Passport used for a trip | Identity & civil status | Travel |
| Child travel consent document | Legal & estate | Travel; education & children |
| Pay statement used during tax filing | Employment & income | Tax; financial |
| Internet installation invoice with equipment details | Household services & utilities | Household assets, receipts & warranties |

The point is not to deny the other connections. It is to avoid turning every connection into another authoritative copy.

## Classification rules

1. **Choose one primary family.** Classify the record by the household context that most naturally owns its ongoing meaning.
2. **Do not classify by file format.** A PDF, photo, email, spreadsheet, or paper form can belong to any family.
3. **Keep secondary meaning as relationships.** A record may relate to several people, properties, trips, assets, accounts, or categories without needing several primary homes.
4. **Do not infer obligations from the taxonomy.** A category or example does not mean every household must have that record or retain it for a particular period.
5. **Treat sensitivity and lifecycle fields as review cues.** They help a household or software system ask better questions; they are not legal, privacy, medical, tax, security, or records-retention rules.
6. **Keep the identifiers stable.** Category IDs are intended to remain stable even if names, examples, display order, or supporting guidance improve over time.

## The fifteen record families

### `ohrt.identity_civil_status` — Identity & civil status
Records that establish identity or significant personal-status facts: passports, birth certificates, citizenship or immigration documents, marriage or divorce records, and name-change records.

### `ohrt.home_property` — Home & property
Records connected to owning, renting, inspecting, improving, repairing, or managing a home or other property: purchase documents, leases, assessments, inspection reports, renovation records, permits, and major property history.

### `ohrt.insurance` — Insurance
Policies, renewals, coverage information, claims, proof of insurance, and insurer correspondence across home, tenant, vehicle, life, travel, and other household insurance.

### `ohrt.tax` — Tax
Returns, notices of assessment or reassessment, tax slips, receipts, and supporting records retained for tax purposes. Tax authorities determine actual filing and retention requirements.

### `ohrt.legal_estate` — Legal & estate
Wills, powers of attorney, representation documents, court records, estate documents, consent documents, and legal agreements.

### `ohrt.emergency_continuity` — Emergency & continuity
Emergency plans, important contacts, care instructions, accessible reference copies, evacuation information, and other material another appropriate person may need when normal household routines are disrupted.

### `ohrt.financial` — Financial
Banking, borrowing, investments, financing agreements, statements, and other household financial records that do not belong more naturally under tax, property, or another specific family.

### `ohrt.vehicles_transportation` — Vehicles & transportation
Registration, purchase and financing records, inspections, maintenance history, service invoices, and other records tied to vehicles or recurring transportation assets.

### `ohrt.health_care` — Health & care
Medication information, vaccination records, benefits documentation, care instructions, dental or vision records, provider information, and other records used to understand or coordinate care.

### `ohrt.household_assets_receipts_warranties` — Household assets, receipts & warranties
Receipts, warranties, manuals, serial numbers, product registrations, repair records, photographs, and other evidence connected to appliances, electronics, furniture, tools, equipment, and other significant belongings.

### `ohrt.education_children` — Education & children
School notices, enrolment records, report cards, permission forms, childcare information, activity registrations, and related education or child records.

### `ohrt.employment_income` — Employment & income
Employment agreements, benefits, pay records, pension documentation, professional credentials, and other records connected to work and household income.

### `ohrt.pets` — Pets
Veterinary records, vaccination information, registrations, insurance, prescriptions, adoption records, licences, and other records associated with household animals.

### `ohrt.travel` — Travel
Itineraries, bookings, visas, travel-insurance records, confirmations, rental documents, and other trip-specific information. Identity documents remain in Identity & civil status even when used for travel.

### `ohrt.household_services_utilities` — Household services & utilities
Electricity, gas, water, internet, mobile service, security systems, recurring home-service agreements, bills, installation records, and related correspondence that may matter during moves, disputes, repairs, or account changes.

## Human workbook and portable data files

[`taxonomy.xlsx`](taxonomy.xlsx) is the human-facing spreadsheet. Its primary **Taxonomy** sheet uses readable column names, wrapped text, practical column widths, frozen headers, filtering, and the human concepts first. A separate **How to Use** sheet explains the classification rule and boundaries. Technical IDs are moved to a secondary **Technical Reference** sheet so they do not dominate the reading experience.

[`taxonomy.csv`](taxonomy.csv) is deliberately a flat portable data export. CSV files cannot store spreadsheet presentation such as column widths, wrapping, colours, frozen panes, fonts, or worksheet layout, so it should not be treated as the designed human spreadsheet.

Each category in `taxonomy.json` includes:

- `id` — stable category identifier;
- `slug` and `name` — human-readable labels;
- `display_order` — presentation hint, not part of identity;
- `definition` — the category boundary in plain language;
- `examples` — illustrative record types, not a requirements list;
- `applicability` — when the family is relevant;
- `sensitivity` — a non-regulatory cue for handling care;
- `lifecycle.review_triggers` — events that should prompt a currency or relevance review;
- `related_categories` — common cross-category relationships.

`taxonomy.schema.json` documents the JSON structure for implementers.

## Versioning

`0.1.0` is the first public review candidate. Stable category IDs are intended to survive normal editorial refinement. A breaking semantic change to category identity or meaning should result in an explicit version change and changelog entry rather than silently reusing an old ID for a different concept.

## Scope and boundaries

OHRT is a reference taxonomy, not a universal checklist of records every household must possess. It is not a Government of Canada taxonomy and does not replace legal, tax, medical, estate-planning, insurance, privacy, security, or jurisdiction-specific guidance.

It also does not require a household or software product to display all fifteen families. The reference model can sit underneath a simpler user interface.

## Licensing status

No reuse license has been assigned to this public review candidate yet. Public visibility should not be interpreted as a blanket permission to reuse or redistribute the taxonomy. Licensing must be resolved deliberately before a final open release.

See [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md) and the repository-wide [`GOVERNANCE.md`](../../GOVERNANCE.md).

## Files

- [`taxonomy.xlsx`](taxonomy.xlsx) — formatted human-facing workbook with Taxonomy, How to Use, and Technical Reference sheets.
- [`taxonomy.json`](taxonomy.json) — canonical machine-readable category data for this candidate.
- [`taxonomy.csv`](taxonomy.csv) — flat portable tabular export for data interchange and simple inspection; not the formatted workbook.
- [`taxonomy.schema.json`](taxonomy.schema.json) — JSON Schema for the published structure.
- [`CHANGELOG.md`](CHANGELOG.md) — version history.
- [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md) — current licensing boundary.
