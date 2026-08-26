# Open Small Business Records Taxonomy

**Version:** 0.1.0  
**Status:** Public review candidate  
**Namespace:** `osbrt`  
**Maintainer:** Eterna Clarity

The Open Small Business Records Taxonomy (OSBRT) is a practical way to decide what a business record is mainly for, which responsibility needs to keep it correct, and what else it should stay connected to.

Its core rule is:

> Give each record one primary category based on the business responsibility that needs the information to stay correct. Keep the other connections as relationships or metadata instead of creating competing primary copies.

OSBRT is not an org chart. A one-person business can use the same model as a larger company: one person may handle finance, sales, purchasing, delivery, and operations, while those responsibilities still remain meaningfully different. The categories describe the work, not the headcount.

The taxonomy is also not a mandated screen layout and it is not the current Clarity Business category interface. A product can show fewer or broader customer-facing categories while mapping records to this richer reference model underneath.

## Start with responsibility, not the file name

A PDF is a file format. `Contract`, `invoice`, `photo`, and `checklist` are record types. Neither reliably tells you which part of the business owns the information.

Ask instead:

**If this record became wrong or disappeared tomorrow, which business responsibility would have to fix the problem?**

Examples:

| Record | Primary family | Useful relationships |
| --- | --- | --- |
| Customer master agreement | Customers & revenue | Finance, accounting & tax; Projects, jobs & delivery |
| Project change order | Projects, jobs & delivery | Customers & revenue; Finance, accounting & tax |
| Supplier agreement | Vendors & procurement | Finance, accounting & tax |
| Purchase invoice | Finance, accounting & tax | Vendors & procurement; Assets & facilities, Inventory & supplies, or Projects, jobs & delivery as applicable |
| Employment agreement | People & workforce | Finance, accounting & tax; Compliance, licences & safety if applicable |
| Equipment maintenance record | Assets & facilities | Vendors & procurement; Finance, accounting & tax if an invoice is related |
| Software service agreement | Technology, access & data | Vendors & procurement; Finance, accounting & tax |
| Safety inspection required by regulation | Compliance, licences & safety | Assets & facilities; Insurance, risk & incidents |

The rule is not “store only one copy under all circumstances.” Accounting, payroll, regulated, contractual, or other systems of record may have their own authority and retention duties. OSBRT is a classification layer: it helps a business identify the record’s primary operational meaning and relate authorized representations without inventing a new authoritative version in every folder.

## When two categories both seem right

1. **Follow the responsibility, not the label.** Do not build catch-all folders called `PDFs`, `Contracts`, `Invoices`, or `Meeting Notes` and assume the job is done. There is intentionally no generic `Contracts` family: a contract stays with the business responsibility it actually governs.
2. **Financial transaction evidence stays financial.** Sales and purchase invoices, receipts, bank records, accounting books, tax support, and remittance evidence belong in **Finance, accounting & tax** when that is their primary purpose.
3. **Relationship is different from delivery.** A master customer agreement or commercial account record belongs in **Customers & revenue**; a scope, work order, change order, field record, or completion package for a specific engagement belongs in **Projects, jobs & delivery**.
4. **Procurement is different from payment.** Supplier selection, purchase orders, supplier agreements, and procurement correspondence belong in **Vendors & procurement**; the resulting purchase invoice normally belongs in Finance.
5. **Workforce is different from payroll accounting.** Employment and contractor relationship records belong in **People & workforce**; payroll journals and remittance evidence belong in Finance when primarily financial.
6. **Assets are different from inventory.** Equipment, vehicles, facilities, maintenance, warranty, inspection, and custody records belong in **Assets & facilities**; stock movement and supply control belong in **Inventory & supplies**.
7. **Risk is different from formal compliance.** Insurance, claims, loss events, and risk records belong in **Insurance, risk & incidents**; licences, permits, required certifications, regulated inspections, and compliance evidence belong in **Compliance, licences & safety** when that obligation is the main reason the record exists.
8. **Technology services can be operationally owned by Technology.** System ownership, access, configuration, recovery, data handling, and technology-service records belong in **Technology, access & data**, even when a vendor and payment are also involved.
9. **Do not use Knowledge as a junk drawer.** **Knowledge & continuity** is only for records whose primary purpose is preserving reusable know-how, decision context, or handoff continuity.
10. **Preserve required authorities.** OSBRT does not displace statutory, contractual, accounting, payroll, privacy, safety, professional, or industry-specific systems of record.

## The fifteen record families

### `osbrt.governance_ownership` — Governance & ownership
Entity formation, ownership, formal authority, governance structure, resolutions, and major company decisions.

### `osbrt.finance_accounting_tax` — Finance, accounting & tax
Accounting books, sales and purchase invoices, receipts, banking, receivables and payables, expenses, reconciliations, financial reports, tax, and financial-remittance records.

### `osbrt.customers_revenue` — Customers & revenue
Leads, proposals, quotes, customer agreements, pricing, commercial correspondence, account records, sales commitments, and recurring customer relationships.

### `osbrt.vendors_procurement` — Vendors & procurement
Supplier profiles, quotes, purchase orders, supplier agreements, price lists, procurement comparisons, credits or returns, receiving exceptions, and vendor correspondence.

### `osbrt.people_workforce` — People & workforce
Employment and contractor agreements, worker profiles, roles, timesheets, training, performance, benefit administration, leave, and other workforce records.

### `osbrt.projects_jobs_delivery` — Projects, jobs & delivery
Work orders, scopes, statements of work, plans, changes, approvals, field records, delivery evidence, completion records, and handoffs for specific work.

### `osbrt.operations_procedures` — Operations & procedures
Recurring operating procedures, checklists, schedules, instructions, quality methods, process controls, and playbooks. Notes and checklists about a specific customer, project, safety obligation, system, or strategic decision belong with that subject instead.

### `osbrt.assets_facilities` — Assets & facilities
Equipment, vehicles, tools, premises, asset registers, manuals, warranties, maintenance, inspections, assignments, repairs, and facility records.

### `osbrt.inventory_supplies` — Inventory & supplies
Item masters, stock counts, receiving, reorder records, usage, movements, adjustments, locations, and recurring material-control records.

### `osbrt.insurance_risk_incidents` — Insurance, risk & incidents
Policies, certificates, claims, incidents, damage evidence, risk assessments, loss records, and risk-management material.

### `osbrt.compliance_licences_safety` — Compliance, licences & safety
Licences, permits, required certifications, regulated inspections, safety-program evidence, compliance filings, corrective actions, and regulatory correspondence.

### `osbrt.technology_access_data` — Technology, access & data
Systems, software subscriptions, account ownership, access procedures, configuration, backup and recovery, data handling, security controls, and technology-service records.

### `osbrt.marketing_brand` — Marketing & brand
Brand standards and assets, campaigns, advertising, photography, content, website or social material, media kits, and publication assets.

### `osbrt.strategy_planning` — Strategy & planning
Business plans, forecasts used for planning, priorities, research, roadmaps, strategic decisions, scenario work, and major initiative direction.

### `osbrt.knowledge_continuity` — Knowledge & continuity
Lessons learned, durable decision context, reference material, handoff notes, process rationale, and information whose primary purpose is preserving what the business knows.

## Recommended record metadata

The taxonomy does not require a particular software system. For implementations, the following fields are useful because they separate classification from operational state:

| Field | Purpose |
| --- | --- |
| `primary_category_id` | Stable OSBRT family that owns the record's primary operational meaning. |
| `record_type` | Human record type such as invoice, quote, work order, agreement, photo, or checklist. |
| `responsible_business_area` | Role, function, or responsibility that owns correctness and follow-up. In a small business, the same person may fill several of these responsibilities. |
| `status` | Current state such as draft, active, completed, superseded, closed, or archived. |
| `sensitivity` | Local handling cue for the specific record; not a legal classification. |
| `review_or_lifecycle_state` | When or why the record should be reviewed, renewed, superseded, or closed. |
| `related_categories` | Other OSBRT families that materially relate to the record. |
| `related_entities` | Relevant customer, vendor, worker, project, asset, account, location, or other business references. |
| `authority_reference` | Pointer to the authoritative system, original, or governing record when the item is a representation or working copy. Do not place passwords, recovery codes, or secrets here. |

## Human workbook and portable data files

[`taxonomy.xlsx`](taxonomy.xlsx) is the human-facing workbook. It opens on **Decision Guide**, which gives the primary question, small-business note, and the main edge cases first. **Taxonomy** keeps the core reading view to five columns: category, meaning, business responsibility, examples, and when to use it. **Category Details** carries handling cues, review triggers, and relationships so the main sheet does not become an eight-column wall of text. **Record Metadata** explains the optional implementation fields, while **Technical Reference** keeps stable IDs and machine-oriented values out of the main reading experience.

[`taxonomy.csv`](taxonomy.csv) is the flat portable export for data interchange. CSV cannot retain spreadsheet presentation such as widths, wrapping, frozen panes, worksheet structure, fonts, or fills, so it is not the designed human spreadsheet.

[`taxonomy.json`](taxonomy.json) is the canonical machine-readable candidate. [`taxonomy.schema.json`](taxonomy.schema.json) documents its structure.

## Scope and authority boundaries

OSBRT is a general small-business classification reference. It is not a Canada Revenue Agency taxonomy and does not replace tax, payroll, corporate, privacy, employment, workplace-safety, professional, contractual, licensing, records-retention, or industry-specific requirements.

The core taxonomy deliberately stays separate from jurisdiction- and industry-specific compliance overlays. A regulated business may need additional classifications, required systems of record, retention schedules, or evidence that this general reference does not define.

Current Canada Revenue Agency guidance confirms that business records can include financial statements, sales invoices, purchase receipts, contracts, work orders, delivery slips, banking records, emails, and supporting correspondence. The CRA determines actual tax record duties and retention requirements; OSBRT does not infer them. See:

- https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/keeping-records.html
- https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/keeping-records/what-records-who-keep-them.html

## Versioning

`0.1.0` is the first public review candidate. Stable `osbrt.*` category IDs are intended to survive normal editorial refinement. Breaking changes to category identity or meaning should be versioned explicitly and recorded in the changelog rather than silently reusing an old identifier for a different concept.

## Licensing status

No reuse license has been assigned to this public review candidate yet. Public visibility should not be interpreted as a blanket permission to copy, modify, redistribute, or incorporate the taxonomy into another product or dataset. Licensing must be resolved deliberately before a final open release.

See [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md) and the repository-wide [`GOVERNANCE.md`](../../GOVERNANCE.md).

## Files

- [`taxonomy.xlsx`](taxonomy.xlsx) — formatted human-facing workbook.
- [`taxonomy.json`](taxonomy.json) — canonical machine-readable category data and implementation guidance.
- [`taxonomy.csv`](taxonomy.csv) — flat portable category export.
- [`taxonomy.schema.json`](taxonomy.schema.json) — JSON Schema for the machine-readable structure.
- [`CHANGELOG.md`](CHANGELOG.md) — version history and review corrections.
- [`LICENSE-NOTICE.md`](LICENSE-NOTICE.md) — current licensing boundary.
