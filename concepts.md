---
title: "Core concepts"
description: "Learn the handful of words webrzn.ru uses everywhere, so the rest of the documentation and the interface stop feeling like a translation."
status: generated
version: "0.1"
---

# Core concepts

Every product has ten or so words that carry its whole model. Learn them once and the rest of the documentation reads like plain English.

Each entry below gives the word, what it is, and the mistake people make about it. That last part is the useful one — definitions are easy, and misunderstandings are what generate support tickets.

> **Fill this in:** replace the entries below with the real nouns from webrzn.ru. Keep the shape — name, definition, common confusion — and keep the list under about ten items. A glossary nobody finishes is a glossary nobody reads.

<!-- widget:accordion -->

### Workspace

The boundary that separates one group's work from another's. Everything else lives inside one.

**Common confusion:** people expect a workspace to behave like a folder. It is closer to an account, and moving things between workspaces is usually deliberate and occasionally impossible.

### Project

A unit of work inside a workspace, with its own settings and history.

**Common confusion:** a project looks like a good place to separate environments. Say whether it is intended that way before somebody splits production and staging across two.

### Source

The place data comes from, together with the credential used to read it.

**Common confusion:** deleting a source rarely deletes what was already imported. State plainly what disappears and what stays.

### Member and role

Who has access, and how much.

**Common confusion:** role names sound like job titles, so people match them to the org chart instead of to the permissions. Write the permissions next to the name — [Invite your team](./guides/invite-your-team.md) has the table.

### Run

One execution of the work, with a start, an end and an outcome you can look at.

**Common confusion:** a run that produced nothing looks identical to a run that never started. Say where run history lives, and what a successful run looks like there.

<!-- /widget -->

## Naming things you create

Two rules save a lot of cleanup later. Put the environment in the name, because "final" and "test" always survive longer than intended. And name things after what they are for rather than who made them — people leave, purposes stay.

<!-- widget:cards plain cols=2 -->

## Next steps

- [What webrzn.ru can do](./features/overview.md) — the vocabulary in use {layers}
- [Import your data](./guides/import-your-data.md) — sources, in practice {database}

<!-- /widget -->
