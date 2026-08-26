# Changelog

All material changes to the Open Household Records Taxonomy should be recorded here.

## 0.1.0 — 2026-08-25

**Status:** Public review candidate

Initial public candidate containing:

- fifteen top-level household record families;
- stable `ohrt.*` category identifiers;
- a primary-classification rule based on household context and future retrieval;
- human-readable category definitions and examples;
- conditional applicability guidance;
- non-regulatory sensitivity cues;
- lifecycle review triggers without invented retention periods;
- common cross-category relationships;
- a formatted human-facing XLSX workbook with Taxonomy, How to Use, and Technical Reference sheets;
- JSON and flat CSV representations for portability and implementation;
- JSON Schema for the machine-readable structure.

### Human spreadsheet correction — 2026-08-25

The original CSV was structurally valid but too technical to serve as the designed human spreadsheet. Because CSV cannot preserve presentation formatting, a dedicated `taxonomy.xlsx` workbook was added. The workbook puts human-readable concepts first, wraps long text, sets practical column widths and row heights, freezes and filters the header, and moves stable IDs/technical fields to a secondary reference sheet. The CSV remains the plain portable export rather than pretending to be the formatted reading experience.

### Final paired validation corrections — 2026-08-25

A final cross-check of the Brief, human workbook and machine-readable package found and corrected several semantic boundaries before 1.0.0:

- **Insurance ownership:** travel and pet insurance policies classify primarily under **Insurance**, with Travel or Pets retained as relationships. Health or supplemental insurance policies are likewise Insurance records.
- **Education coverage:** **Education & children** explicitly covers education and training records for household members generally, including post-secondary enrolment, transcripts, diplomas and certificates, while retaining child/dependant school, childcare and activity administration where that is the record's primary purpose.
- **Domain-specific agreements and financing:** specific household context now takes precedence over generic document type. Leases remain Home & property records; vehicle financing remains Vehicles & transportation; employment agreements remain Employment & income. **Legal & estate** is reserved for records whose main purpose is personal legal authority, status, representation, court matters or estate matters, and **Financial** is reserved for general financial records that do not belong more naturally in a specific domain.
- **Coverage, employment benefits and care:** insurance policies stay in **Insurance**; employment-benefit enrollment or plan administration stays in **Employment & income**; medical, treatment, medication, provider and care records stay in **Health & care**.
- **Sensitivity cue refinement:** **Education & children** moved from a blanket `highly_sensitive` category cue to `often_sensitive`, with the note preserving the higher-risk considerations that can apply to records involving children, custody, location, care or accommodations.

The README, JSON, CSV and XLSX were synchronized to these corrections and revalidated against the same 15-category model.

### Review boundaries before 1.0.0

- confirm the final reuse license;
- validate category boundaries and edge cases against varied realistic household scenarios;
- verify that the stable identifiers are suitable for long-term public use;
- review machine-readable fields for unnecessary complexity or missing implementation needs;
- ensure the human-readable and machine-readable representations remain semantically aligned.
