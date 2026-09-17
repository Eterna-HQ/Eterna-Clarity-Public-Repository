# CSV Import Check

**Version 1.0.1.** A plain-language preflight for spotting CSV values that may be changed, misread, or rejected when you import them into a spreadsheet, CRM, accounting tool, or another app.

A CSV can open normally and still contain data that gets interpreted differently during import. Common examples include account numbers with leading zeros, very long numeric identifiers, cells that look like formulas, duplicate column names, or rows with the wrong number of fields.

This resource helps you look for those problems before the import.

## What to check

The companion browser tool is designed to flag things such as:

- blank or duplicate column names;
- rows with more or fewer fields than the header;
- values such as `001234` where a leading zero may matter;
- long digit-only identifiers that a spreadsheet may change or display differently;
- cells beginning with formula-style characters such as `=`, `+`, `-`, or `@` when they may be interpreted instead of treated as plain text;
- exact duplicate values in a column you choose to treat as an identifier. Spaces are preserved when comparing; a missing key is reported separately.

The tool reports the row, column, original value, and a simple explanation. It does not rewrite the CSV for you.

## Use the checklist without the tool

[Open the CSV import checklist](IMPORT-CHECKLIST.md) and use it before a real import.

The [fictional example](EXAMPLE.md) shows the kind of issue the checker is meant to catch.

## Important limits

This is not a guarantee that a CSV is safe or compatible with every app. Import behaviour varies by software and version. Use the destination application's current import instructions, keep the original CSV, and test a small copy before changing important data.

The checker should not guess missing digits, repair identifiers, or decide that a suspicious-looking value is definitely dangerous. It should show you the original value and explain why it deserves a look.

## Privacy

The browser checker reads the CSV locally in your browser. It does not need an Eterna account or a backend upload.

## Reuse

The original checklist, example and documentation in this folder are licensed under [CC BY 4.0](LICENSE-NOTICE.md). Application code is separate and is not released under this content licence.

See [SOURCES.md](SOURCES.md) for the specific evidence behind the checks and their limits.

## File format and errors

Use comma-separated UTF-8 text, up to 5 MB, 100,000 rows and 10,000 columns. Quoted commas, doubled quotes and line breaks inside quoted fields are supported. An unclosed quote, stray quote, invalid UTF-8 or an empty file produces a clear message rather than retaining a previous result. Files with another encoding or delimiter must be exported appropriately first.

An ordinary negative number, such as `-12.5`, is not flagged merely for beginning with a minus sign. A warning about a long identifier or formula-looking value is a reason to inspect it, not proof that it has already changed or is unsafe. The report shows up to 200 findings and says when additional findings were omitted.
