# CSV Import Checklist

Use this before importing an important CSV into another app.

## Keep the original

Make a copy for testing. Do not overwrite your only copy while fixing import problems.

## 1. Check the column names

Look for:

- blank column names;
- two or more columns with the same name;
- unexpected extra columns;
- names the destination app does not recognize.

## 2. Check rows that do not match

A normal row should usually have the same number of fields as the header.

Look for rows with extra or missing fields. Quoted cells can contain commas and line breaks, so use a proper CSV reader rather than simply splitting each line at commas.

## 3. Protect identifiers

Look for values where the exact text matters, especially:

- postal codes;
- employee or customer IDs;
- account numbers;
- product codes;
- tracking numbers;
- other identifiers that may begin with zero.

A value such as `001234` is not always the same thing as the number `1234`.

Also review long digit-only values. Some spreadsheet software can display or store long numbers differently from the original text.

## 4. Review formula-looking cells

If a cell begins with characters such as `=`, `+`, `-`, or `@`, check whether it is supposed to be ordinary text or something the destination application may interpret.

Do not automatically remove characters. A negative number such as `-12.50` may be completely legitimate. The useful action is to review the original value in context.

## 5. Check identifiers for duplicates

If one column is supposed to contain unique IDs, emails, invoice numbers, SKU values or another unique key, check for exact duplicates before importing.

Do this only when uniqueness is actually expected.

## 6. Test a small import first

Before importing thousands of rows:

1. make a small representative test file;
2. include a few known identifiers, dates, blank values, long numbers and other edge cases that matter to you;
3. import it into the destination;
4. compare the result with the original CSV;
5. only then decide whether to proceed with the full file.

## Do not treat a clean checklist as a guarantee

Different apps interpret CSV files differently. A preflight can show common problems, but it cannot certify compatibility with every import screen, locale, version or destination rule.

Original checklist by Eterna Clarity. See `LICENSE-NOTICE.md` for reuse terms.
