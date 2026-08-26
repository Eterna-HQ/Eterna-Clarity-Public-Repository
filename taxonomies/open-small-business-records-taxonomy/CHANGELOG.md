# Changelog

All material changes to the Open Small Business Records Taxonomy should be recorded here.

## 0.1.0 — 2026-08-25

**Status:** Public review candidate

Initial public candidate containing:

- fifteen top-level small-business record families;
- stable `osbrt.*` identifiers;
- an accountability-based primary-classification rule;
- explicit tie-breakers for contracts, invoices, customer vs project records, procurement vs payment, workforce vs payroll, assets vs inventory, risk vs compliance, technology services, strategy, and knowledge;
- human-readable definitions, examples, applicability guidance, sensitivity cues, lifecycle review triggers, and common relationships;
- recommended record metadata separating category, record type, responsibility, lifecycle, relationships, and authority reference;
- a formatted human-facing XLSX workbook with Taxonomy, Decision Guide, Record Metadata, Technical Reference, and References sheets;
- JSON and CSV representations;
- JSON Schema for the machine-readable structure.

### Design corrections made during asset implementation

The asset implementation tightened several boundaries from the earlier editorial description before public release:

- generic `contract`, `invoice`, `meeting notes`, and `checklist` buckets are explicitly rejected as primary categories;
- transaction evidence such as sales and purchase invoices is owned by Finance, accounting & tax when its primary purpose is accounting or tax support;
- customer commercial relationship records are separated from delivery records for a specific project or job;
- supplier/procurement records are separated from resulting financial transaction evidence;
- employment/contractor relationship records are separated from payroll journals and remittance evidence;
- recurring operating methods are separated from topic-specific notes, project plans, compliance evidence, and strategic planning;
- physical asset records are separated from inventory-control records;
- incident/risk records are separated from formal licence, inspection, certification, and compliance evidence;
- technology-service records can be owned by Technology, access & data when their primary operational purpose is the system or service;
- mandatory external systems of record are explicitly preserved rather than displaced by the taxonomy.

### Review boundaries before 1.0.0

- founder paired review and approval of the final Brief plus this asset;
- confirm the final reuse license;
- validate category boundaries against varied realistic small-business scenarios and industries;
- verify stable identifiers for long-term public use;
- confirm that general core categories remain distinct from jurisdiction- and industry-specific compliance overlays;
- ensure the human-readable and machine-readable representations remain semantically aligned.
