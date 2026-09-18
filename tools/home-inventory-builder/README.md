# Home Inventory Builder

List your belongings room by room, note where photos or receipts are kept, and save a copy for later. Values are amounts you choose to record, not insurance valuations or replacement-cost estimates.

[Use the browser tool](https://staging.eterna-clarity-portal.pages.dev/resources/home-inventory/) | [Blank CSV](INVENTORY-TEMPLATE.csv) | [Fictional CSV example](EXAMPLE.csv) | [Reopenable fictional example](EXAMPLE.json)

## Start and come back later

Choose one currency code for the whole inventory, such as CAD. Add a room and item; the other details are optional. Enter amounts such as `1200` or `1,200.50`. Changing the currency label does not convert amounts.

Use **Edit** to correct an entry. Add or save the current entry before exporting. **Save data file** creates a JSON file containing your recorded entries. Keep that file somewhere private. On a later visit, choose **Open saved data** to continue. Opening a saved file replaces the records in the tool after confirmation; it does not merge two inventories.

Your work stays in the current tab while you browse Resources, but it is not automatically saved across a refresh or closed tab. Do not rely on a browser warning as your only reminder to save.

**Download CSV** creates an eight-column table for a spreadsheet. It is not the format used to reopen the browser tool. Import serial numbers as text in the receiving app so identifiers such as `001234` remain intact. The tool does not attach or upload your photos or receipts; it records where you keep them.

Saved files may contain up to 10,000 entries and be no larger than 5 MB. Each text field may contain up to 10,000 characters. The tool reports a problem rather than silently replacing an invalid amount with zero.

## Privacy and reuse

Records are processed in your browser, not sent to Eterna. A completed inventory is still private information; avoid unnecessary identity or account details and keep downloaded copies secure.

[Sources](SOURCES.md) | [Licence notice](LICENSE-NOTICE.md). No open reuse licence has been assigned to this companion package.
