---
title: "Troubleshooting"
description: "Work out what went wrong in webrzn.ru in the right order, fix the common causes yourself, and know exactly what to send if you need help."
status: generated
version: "0.1"
---

# Troubleshooting

Work through this page in order. Most problems are caught in the first section, and the later sections are much more work.

## First, establish what actually happened

Three questions, in this order:

1. **What did you expect?** Write it in one sentence. Half of all reported bugs dissolve here.
2. **What happened instead?** The exact message, copied rather than paraphrased. Error text is searchable; "it didn't work" is not.
3. **When?** A timestamp with a time zone. Logs are indexed by time, and "this morning" spans four hours.

## The usual causes

<!-- widget:accordion -->

### It works for you and fails for a colleague

Almost always permissions. Compare roles rather than accounts — two people in the same team can hold different ones, and the difference is invisible from the outside. See [Invite your team](./guides/invite-your-team.md).

### It worked yesterday and fails today

An expired or rotated credential. Re-issue the token, retry once, and check whether it belongs to the environment you think it does.

### It works on small input and fails on large

A limit: size, rate or timeout. Retry with a fraction of the input. If the small version succeeds, you have found the shape of the problem without reading a log.

### The answer is right but the numbers are wrong

Time zone or locale. Compare one record against the source by hand before suspecting anything more complicated. See [Import your data](./guides/import-your-data.md).

### Nothing happened at all

Silence is its own category. Check, in order: whether the job started, whether it is waiting on something, and whether it finished and wrote its output somewhere you are not looking. A run that produced no records and a run that never ran look identical from outside.

<!-- /widget -->

> **Fill this in:** where a reader sees run history in webrzn.ru, and what a successful run looks like there. This is the single most useful thing on the page, and only you can write it.

## When to ask for help

Ask once you have the three answers from the first section. Send them together with what you already tried, and say what would unblock you — an answer, a workaround, or a fix. That last sentence changes how quickly the right person picks it up.

> **Fill this in:** the support address or form, and a realistic response time. A promise you cannot keep is worse than no promise.

<!-- widget:cards plain cols=2 -->

## Next steps

- [FAQ](./faq.md) — the questions that come up right after setup {circle-help}
- [Getting started](./getting-started.md) — retrace the setup {rocket}

<!-- /widget -->
