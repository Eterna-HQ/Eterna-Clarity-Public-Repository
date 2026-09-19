# What Does Your Business Depend On?

A simple way to map the people, systems, data and outside providers that one important business activity depends on.

[Use the browser tool](https://eternaclarity.com/resources/business-dependency-map/) · [Open the plain template](DEPENDENCY-TEMPLATE.md) · [See a fictional example](EXAMPLE.md)

## What this is

Choose a business activity that matters, such as invoicing customers, scheduling work, taking payments or delivering a service. Then list the things that activity depends on.

For each dependency, record:

- what the activity is;
- the person, system, data, supplier or other dependency;
- what would happen if it were unavailable;
- who normally owns or controls it;
- the backup person, alternate provider or fallback path;
- whether that fallback has actually been tested; and
- when you last checked it.

The useful result is not a giant inventory. It is a short list of dependencies that could stop important work because no practical fallback exists.

## Keep secrets out

Do **not** record passwords, recovery codes, API keys, private keys, full payment credentials or other secrets. Point to the approved place where access is managed instead.

## Prove one fallback

Pick one dependency that would stop the activity and test the stated fallback without disrupting live work. If the alternate person, system or path cannot actually support the task, treat the fallback as unproven.

## Important limits

This is a practical dependency-mapping resource, not a complete business continuity plan, cyber-security assessment, supplier-risk assessment, legal review or guarantee that the business can continue through every disruption.

See [SOURCES.md](SOURCES.md) for the Canadian guidance used to define the problem and boundaries.

## Reuse

No open reuse licence has been assigned to this companion package. See [LICENSE-NOTICE.md](LICENSE-NOTICE.md).
