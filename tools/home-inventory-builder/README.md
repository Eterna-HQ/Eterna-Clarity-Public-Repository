# Home Inventory Builder

List belongings room by room, note where photos or receipts are kept, and save a copy to continue later.

[Preview the browser tool](https://staging.eterna-clarity-portal.pages.dev/resources/home-inventory/) (staging review; access may be required). The public library remains [Resources](https://eternaclarity.com/resources/).

## Start here

Add the room and item. Brand, model, serial number, purchase date, amount and photo or receipt location are optional. Edit an entry to correct it, or remove an entry you no longer need.

Choose the currency used by the amounts, such as CAD. Amounts accept `1200` or `1,200.50`; an empty amount stays empty and zero stays zero. A currency label does not convert values. The total adds the amounts you recorded; it is not an insurance valuation or an estimate of replacement cost.

## Files you can use

- [Blank CSV](INVENTORY-TEMPLATE.csv) and [fictional CSV example](EXAMPLE.csv): eight columns, including currency.
- [Blank saved-data file](INVENTORY-TEMPLATE.json) and [fictional saved-data example](EXAMPLE.json): open these with **Open saved data** in the browser tool.
- [Sources](SOURCES.md) and [licence notice](LICENSE-NOTICE.md).

## Keep your information private

The browser tool keeps entered records in the current tab. It does not send their contents to Eterna or save them automatically to an account. Download a data file before leaving or refreshing the page. Keep saved files somewhere private, particularly on a shared device.

Use **Save data file** and later **Open saved data** to continue. A CSV is for viewing in a spreadsheet; it cannot be reopened as a saved record in this tool. Finish or discard the current form entry before downloading. Opening a different saved file replaces the tool's current records after confirmation.

The tool accepts its matching JSON data format, up to 5 MB and 10,000 records. Invalid files leave the current records unchanged.

## Version and reuse

Companion edition 1.0.1, reviewed 17 September 2026. The saved-data format remains `eterna.home-inventory.v1`. Older matching files without a currency can be opened; select their currency before relying on a total. No new reuse licence is granted by this maintenance edition.
