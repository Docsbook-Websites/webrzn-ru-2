---
title: "Security and data"
description: "Answer the questions a security reviewer asks about webrzn.ru: who can see what, where data lives, how long it is kept and how to get it out."
status: generated
version: "0.1"
---

# Security and data

This page exists so a buyer's security review can be answered from a URL instead of a questionnaire. Write it once, keep it accurate, and send the link.

<!-- widget:callout type=note -->

Every answer below should be one you can defend. A vague "industry-standard encryption" invites a follow-up; a specific "encrypted in transit with TLS 1.2 or later, and at rest by the storage provider" ends the conversation.

<!-- /widget -->

## Who can see what

Access follows the role. Write down which roles exist, what each one can read, and what each one can change — [Invite your team](./guides/invite-your-team.md) has the same table from the administrator's side.

> **Fill this in:** the roles, and any data a role cannot see at all. Reviewers look specifically for whether support staff can read customer content.

## Where data lives

Name the regions your data is stored in, and say whether a customer can choose. If it leaves that region for any reason — a backup, a support tool, a sub-processor — say so here rather than leaving it to be discovered.

> **Fill this in:** regions, sub-processors, and whether a data processing agreement is available.

## How long it is kept

| Kind of data | Kept for | Deleted when |
| --- | --- | --- |
| Records you import | Fill this in | Fill this in |
| Run history and logs | Fill this in | Fill this in |
| Backups | Fill this in | Fill this in |
| Account after cancellation | Fill this in | Fill this in |

A retention table with four honest rows is worth more than a page of assurance. It is also the section customers come back to years later, so keep it current.

## Getting your data out

Say which formats are available, who can trigger an export, and how long a full export takes. An export route that exists only as a support request is worth documenting as exactly that — readers trust a specific inconvenient answer more than a comfortable vague one.

## Reporting a vulnerability

> **Fill this in:** the address to report to, whether you run a disclosure programme, and how quickly you acknowledge a report. Researchers who cannot find this page post publicly instead.

<!-- widget:cards plain cols=2 -->

## Next steps

- [Invite your team](./guides/invite-your-team.md) — roles in practice {users}
- [FAQ](./faq.md) — the short versions of these answers {circle-help}

<!-- /widget -->
