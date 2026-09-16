# Sources and limits

Observed 16 September 2026.

This resource focuses on a few CSV problems that are easy to miss before import. It is not a complete rulebook for every spreadsheet, CRM, accounting product or locale.

## Official examples

- Microsoft, [Keeping leading zeros and large numbers](https://support.microsoft.com/en-us/office/keeping-leading-zeros-and-large-numbers-1bf7b935-36e1-4985-842f-5dfa51f85fe7): Excel can interpret text-like identifiers and long numeric strings in ways that change their displayed or stored form. Import behaviour depends on the method and available settings.
- Microsoft, [Data import and analysis options](https://support.microsoft.com/en-US/Excel/data-import-and-analysis-options-in-excel): automatic conversion behaviour is affected by Excel's import and conversion settings. This is one reason a checker should flag patterns for review rather than claim to predict every application.
- OWASP Community, [CSV Injection](https://community.owasp.org/attacks/CSV_Injection): spreadsheet applications can interpret some cell values beginning with formula characters. A checker can identify formula-looking input, but context matters and no single automatic rewrite is universally correct.

These sources do not endorse this resource. Their content is not included in this resource's reuse licence, and software behaviour can change.

## What this does not establish

A CSV that produces no warnings is not certified safe, clean or compatible with a particular destination.

This resource does not:

- know every destination application's schema or business rules;
- know whether leading zeros or duplicate values are intentional in your data;
- guarantee how a particular spreadsheet version or locale will interpret every value;
- sanitize untrusted spreadsheet content;
- recover digits or characters that were already lost before the CSV reached the checker;
- automatically repair or rewrite the user's source file.

The useful result is a short list of values and rows worth checking before a real import.
