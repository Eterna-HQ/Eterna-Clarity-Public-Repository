# Business dependency map

Start with **one important business activity**.

Do not put passwords, recovery codes, API keys or other secrets in this file.

| Important activity | Dependency | Type | If unavailable | Owner / role | Backup or alternate path | Fallback tested? | Last checked |
| --- | --- | --- | --- | --- | --- | --- | --- |
|  |  | Person / System / Data / Vendor / Physical / Other | Would stop / Would slow / Manageable |  |  | Yes / No / Not sure / Does not apply |  |

## What to fix first

Start with dependencies that:

1. would **stop** the activity;
2. have no named backup or alternate path; or
3. have a fallback marked **No** or **Not sure**.

## Proof step

Choose one high-impact dependency and test the fallback safely. The useful question is:

**Can the business still perform the activity using the stated fallback?**

If not, the fallback is not ready yet.
