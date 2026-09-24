---
title: "Integrations"
description: "Connect webrzn.ru to the tools your team already uses, so results arrive where people work instead of in another tab nobody opens."
status: generated
version: "0.1"
---

# Integrations

An integration is worth building when it removes a tab somebody opens every day. List here what webrzn.ru connects to, and be honest about which direction the data flows.

<!-- widget:cards cols=2 -->

- [Chat and notifications](./guides/invite-your-team.md) — Push results to the channel where decisions get made {message-square}

  One-way, and that is usually right: a notification that can also change state turns a chat room into an admin panel.

- [Data sources](./guides/import-your-data.md) — Read from the systems that already hold your records {database}

  Two-way if you write back, and that is the connection to document most carefully.

<!-- /widget -->

> **Fill this in:** replace the two cards above with the integrations webrzn.ru really ships, and add one card per integration. An integration page that lists something you have not built is the most expensive kind of wrong.

## Connect over the API

Where no first-party integration exists, the API is the answer. Show the same call in the shapes your readers use.

<!-- widget:code-group -->

Both variants send the same request and get the same response back.

```bash
curl -X POST "https://api.example.com/v1/events" \
  -H "Authorization: Bearer $API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"type": "report.ready", "project": "first-project"}'
```

```js
await fetch("https://api.example.com/v1/events", {
  method: "POST",
  headers: {
    Authorization: "Bearer " + process.env.API_TOKEN,
    "Content-Type": "application/json",
  },
  body: JSON.stringify({ type: "report.ready", project: "first-project" }),
})
```

<!-- /widget -->

## What to write about each integration

Four things, and most integration pages skip the last two: what it does, how to connect it, what happens when the other side is unavailable, and how to disconnect it cleanly. The last one matters because somebody eventually has to, usually in a hurry.

<!-- widget:cards plain cols=2 -->

## Next steps

- [Security and data](./security.md) — what an integration can reach {shield}
- [Troubleshooting](./troubleshooting.md) — when a connection stops delivering {wrench}

<!-- /widget -->
