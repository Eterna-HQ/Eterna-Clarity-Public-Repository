# Insurance Claim Log

Keep your claim number, conversations, expenses and next steps in one place.

[Preview the browser tool](https://staging.eterna-clarity-portal.pages.dev/resources/insurance-claim-log/) (staging review; access may be required). The public library remains [Resources](https://eternaclarity.com/resources/).

## Use the log

Add claim details at the top, then record an item or damage, a conversation, an expense or a next action. Entries are shown by date. Entries on the same date keep their recorded order. Edit an entry to correct it or note that an action has been completed; this is a timeline, not a separate task-management system.

Choose the currency used in this claim. Amounts accept `1200` or `1,200.50`; a blank amount stays blank. The expense total includes only entries marked **Expense**. It is not an insurer's decision about what will be paid. Follow your insurer's instructions for what to submit.

## Files you can use

- [Blank CSV](CLAIM-LOG-TEMPLATE.csv) and [fictional CSV example](EXAMPLE.csv): a consistent ten-column table. Claim details and currency are repeated on each row so the export remains a usable data table.
- [Blank saved-data file](CLAIM-LOG-TEMPLATE.json) and [fictional saved-data example](EXAMPLE.json): preserve claim details and entries for reopening in the browser tool.
- [Sources](SOURCES.md) and [licence notice](LICENSE-NOTICE.md).

The browser also offers a readable text report. Do not confuse that report with the CSV data table.

## Keep your information private

The browser tool keeps entered records in the current tab. It does not send their contents to Eterna or save them automatically to an account. Download a data file before leaving or refreshing the page. Keep saved files somewhere private, particularly on a shared device.

Use **Save data file** and later **Open saved data** to continue. A CSV is for viewing in a spreadsheet; it cannot be reopened as a saved record in this tool. Finish or discard the current form entry before downloading. Opening a different saved file replaces the tool's current records after confirmation.

The tool accepts its matching JSON data format, up to 5 MB and 10,000 records. Invalid files leave the current records unchanged.

## Version and reuse

Companion edition 1.0.1, reviewed 17 September 2026. The saved-data format remains `eterna.insurance-claim-log.v1`. No new reuse licence is granted by this maintenance edition. Do not include real claim records in public examples or issue reports.
