# Account Recovery Check

Check how you would get back into important accounts if you lost your phone or usual sign-in method.

[Preview the browser check](https://staging.eterna-clarity-portal.pages.dev/resources/account-recovery-check/) (staging review; access may be required), or use the [plain checklist](CHECK.md).

## What to record

Use a plain account label, such as "Primary email", rather than a password or recovery code. For each account, choose **Yes**, **No** or **Not sure** for whether you could recover it without the main phone, whether the recovery contact is up to date, and whether another way in is available. No answer is selected for you.

Any **No** produces an attention warning, including an outdated recovery contact. **Not sure** is reported separately and can overlap with accounts already needing attention. These are your answers, not proof that recovery will work.

The backup-method note is a reminder to check dependencies yourself. The tool does not infer an account-dependency graph from names or claim to test a recovery process.

## Files you can use

- [Checklist](CHECK.md) and [fictional written example](EXAMPLE.md).
- [Blank saved-data file](RECOVERY-TEMPLATE.json) and [fictional saved-data example](EXAMPLE.json), for **Open saved data**.
- [Sources](SOURCES.md) and [licence notice](LICENSE-NOTICE.md).

## Keep your information private

The browser tool keeps entered records in the current tab. It does not send their contents to Eterna or save them automatically to an account. Download a data file before leaving or refreshing the page. Keep saved files somewhere private, particularly on a shared device.

Use **Save data file** and later **Open saved data** to continue. A CSV is for viewing in a spreadsheet; it cannot be reopened as a saved record in this tool. Finish or discard the current form entry before downloading. Opening a different saved file replaces the tool's current records after confirmation.

The tool accepts its matching JSON data format, up to 5 MB and 10,000 records. Invalid files leave the current records unchanged.

Never enter passwords, recovery codes, PINs or security answers. Use the account provider's own instructions to set up or check recovery.

## Version and reuse

Companion edition 1.0.1, reviewed 17 September 2026. The saved-data format remains `eterna.account-recovery-check.v1`. No new reuse licence is granted by this maintenance edition.
