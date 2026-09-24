---
title: "Import your data"
description: "Bring a real source into webrzn.ru safely — start small, check what actually arrived, and widen the import only once the sample is right."
status: generated
version: "0.1"
---

# Import your data

Importing real data is the step where webrzn.ru stops being a demonstration. It is also the step most likely to go wrong in a way nobody notices, so this guide is built around checking rather than around importing.

<!-- widget:callout type=warning -->

Do not start with your largest source. Sample data proves the connection works and nothing about whether it works on your material — which is where the surprises live: an unusual character set, a column that is empty half the time, a date written the American way.

<!-- /widget -->

<!-- widget:stepper -->

### Create a narrow credential

Scope it as tightly as the source system allows. Read-only, if reading is all that is needed, and store it where your team already keeps secrets.

### Name the connection after what it is

Include the environment. A connection called "test" outlives every test.

### Run the import once, by hand

Schedule nothing until you have seen one result.

```json
{
  "name": "orders-staging",
  "source": "https://data.example.com/exports/orders",
  "auth": { "type": "bearer" },
  "schedule": null
}
```

### Check three things by eye

Count, edges and ugly rows — the table below says what each one catches.

<!-- /widget -->

> **Fill this in:** replace the example above with the real shape webrzn.ru expects, and say which fields are required.

## What to check, and what a failure looks like

| Check | How | What a failure looks like |
| --- | --- | --- |
| Count | Compare the number of records against the source | Off by a round number, usually a page limit |
| Edges | Open the oldest and the newest record | Timestamps shifted by a fixed number of hours: a time zone |
| Ugly rows | Find a record with accents, emoji or an empty field | Question marks, truncation, or a silent skip |

Do not trust a green tick on its own. An import that reports success and drops a tenth of the rows looks exactly like one that worked.

## Then widen it

Once the small source is right, add the rest one at a time, repeating the same three checks after each. Connecting six at once means debugging six at once.

<!-- widget:cards plain cols=2 -->

## Next steps

- [Integrations](../integrations.md) — where the output can go next {plug}
- [Troubleshooting](../troubleshooting.md) — when an import refuses {wrench}

<!-- /widget -->
