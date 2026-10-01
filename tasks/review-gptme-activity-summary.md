---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-activity-summary with Skogix

Walk through `gptme activity-summary` together and decide how it fits dot's workflow.
Listed as an installed external command by `gptme --help` on 2026-10-02;
functional behavior has not yet been validated.

## Walkthrough

- [ ] Inspect installed version, executable location, CLI help, and dependencies.
- [ ] Explain agent journal mode versus human ActivityWatch mode and daily/weekly/monthly reports.
- [ ] Demonstrate a raw report from a small, explicitly selected fixture or approved date range.
- [ ] Review optional GitHub/ActivityWatch sources, LLM synthesis, costs, and retained private traces.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively, one package at a time. Do not read unrelated email or
activity history, invoke an LLM backend, or enable scheduling without approval.
Prefer synthetic journals and raw output first. Finish when the walkthrough and
decision are recorded in a new journal entry, with repeatable commands and any
blockers; installation alone is not validation.

## Reference

- [Package documentation](../gptme-contrib/packages/gptme-activity-summary/README.md)
