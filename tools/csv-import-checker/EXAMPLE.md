# Example: a customer list that looks fine until import

This example is fictional.

A small organization exports a customer list before moving it into a new CRM.

The CSV opens and appears normal at first glance:

```csv
customer_id,name,account_ref,email
001204,Asha Patel,78210451987654321,asha@example.test
001205,Mark Chen,=IMPORT("old"),mark@example.test
001205,Rina Bell,55007,rina@example.test
001207,Noah Green,44120,noah@example.test,unexpected-extra-field
```

A useful checker would call attention to four things without changing the file:

| Where | Original value | Why look at it |
| --- | --- | --- |
| Row 2, `customer_id` | `001204` | The leading zeros may matter if this is an identifier rather than a number. |
| Row 2, `account_ref` | `78210451987654321` | This long digit-only value should be checked after spreadsheet import to make sure the exact text was preserved. |
| Row 3, `account_ref` | `=IMPORT("old")` | It begins like a formula. Confirm that the destination treats it the way you intend. |
| Rows 3 and 4, `customer_id` | `001205` | The ID is duplicated. That matters only if this column is supposed to be unique. |
| Row 5 | extra field | The row has more fields than the header. The destination may reject or misalign it. |

The checker should not “fix” these values automatically.

For example, changing `001204` to `1204` could destroy the identifier. Removing the leading `=` from a value might also change legitimate data. The right first step is to show the original value, explain the risk in plain language, and let the user decide what the destination expects.
