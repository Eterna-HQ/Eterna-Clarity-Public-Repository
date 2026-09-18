# CSV Import Check

Check a CSV for missing column names, uneven rows and values another app might change.

[Use the browser checker](https://eternaclarity.com/resources/csv-import-check/) | [Read the import checklist](IMPORT-CHECKLIST.md) | [Fictional example](EXAMPLE.md)

## What it checks

Choose a comma-separated UTF-8 file. The checker reports blank or repeated column names, uneven records, leading-zero values, long digit-only values and formula-looking text. An empty file, invalid UTF-8 or a malformed quoted field produces an error instead of keeping the previous file's result.

The optional key-column check compares values exactly, including spaces and letter case. `A`, ` A` and `a` are different values. Missing key values are reported separately. Column-name comparisons, unlike key values, ignore surrounding spaces and case.

A quoted value can contain commas, doubled quotes or newlines. Row numbers count CSV records, not physical text lines. Blank rows and spaces in values are preserved.

The browser limit is 5 MB, 100,000 data rows and 10,000 columns. At most 200 findings are displayed, but the total includes all findings found. Long value previews are shortened without changing the original file.

## Understand the warnings

A leading zero may be meaningful in an identifier. A long number may be reformatted by another app. Formula-looking text needs review, but an ordinary negative number is not automatically an unsafe value. A warning is not proof that data has already changed or that a value is dangerous.

The checker does not change your file, infer missing digits or guarantee acceptance by every app. Keep the original, follow the receiving app's import instructions and test a small copy before changing important data.

## Privacy and reuse

The file is read locally in your browser, not uploaded to Eterna. No account is required.

The checklist, fictional example and documentation retain their existing [CC BY 4.0 terms](LICENSE-NOTICE.md). Browser application code is separate from that content licence. See [SOURCES.md](SOURCES.md) for background.
