# Fictional example — Business dependency map

This example uses a fictional small design studio.

| Important activity | Dependency | Type | If unavailable | Owner / role | Backup or alternate path | Fallback tested? | Last checked |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Send customer invoices | Accounting service | System | Would stop | Owner | Manual invoice template and current customer list | No | 2026-09-12 |
| Send customer invoices | Current customer records | Data | Would stop | Operations | Exported monthly copy in shared Finance folder | Yes | 2026-09-12 |
| Send customer invoices | Bookkeeper | Person | Would slow | Bookkeeper | Owner knows the billing sequence | Not sure | 2026-09-12 |
| Receive website enquiries | Website form provider | Vendor | Would slow | Owner | Public email address | Yes | 2026-09-12 |

The highest-priority gap is the untested manual invoicing fallback because the accounting service is marked **Would stop**.
