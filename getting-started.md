---
title: "Getting started"
description: "Go from a new webrzn.ru account to a working setup in one sitting, with a checkpoint after every step so you know it worked."
status: generated
version: "0.1"
---

# Getting started

Every step below ends with a checkpoint: something you can look at to confirm it worked. If a checkpoint fails, stop there — the next step will not fix it.

<!-- widget:callout type=note -->

### Before you begin

You need an account, permission to create a project, somewhere safe to keep a credential, and fifteen uninterrupted minutes.

<!-- /widget -->

> **Fill this in:** the real prerequisites — a supported runtime version, a minimum plan, an admin role. Readers forgive a long list at the top; they do not forgive finding out about one halfway through.

<!-- widget:stepper -->

### Create a project

Sign in and create your first project. Give it the name your team already uses for this work rather than a test name — first projects have a habit of becoming production.

**Checkpoint:** the project appears in the sidebar under a name you recognise.

### Connect something real

A product like this only becomes useful once it is pointed at your own data. Do that now, with a small, low-risk source rather than your largest one.

```bash
export API_TOKEN="paste-your-token-here"

curl -X POST "https://api.example.com/v1/projects" \
  -H "Authorization: Bearer $API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"name": "first-project", "source": "sandbox"}'
```

**Checkpoint:** the response carries an id, and the project shows the connection as active.

### Run the core workflow once

Do the thing the product is for, end to end, against that small source. Resist configuring anything else until you have seen one result.

**Checkpoint:** you can point at an output and say what produced it.

### Save the setup for your team

Write down which credential you used and where it lives. The person who repeats this next month is usually not you.

**Checkpoint:** a colleague could redo these steps from your note alone.

<!-- /widget -->

> **Fill this in:** replace the host, the path and the fields in step two with a request that actually works, and say what a successful response looks like.

## When a step fails

Read the error text before changing anything — most setup errors name the field they object to. Then check the three usual suspects: the credential belongs to a different environment, the account is missing a permission, or a required field was left empty. [Troubleshooting](./troubleshooting.md) goes through them in order.

<!-- widget:cards plain cols=2 -->

## Next steps

- [Core concepts](./concepts.md) — the words you just met, defined {compass}
- [Invite your team](./guides/invite-your-team.md) — add the people who will use it daily {users}

<!-- /widget -->
