---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-sessions with Skogix

Walk through `gptme sessions`, listed by `gptme --help` on 2026-10-02.
Review cross-harness session discovery, stored records, and analytics.
Installed command discovery is not functional validation.

## Walkthrough

- [ ] Inspect installed version, CLI help, store defaults, and discovery scope.
- [ ] Explain native trajectory discovery versus the append-only session store and distinguish stats from LLM judging.
- [ ] Use synthetic records in an isolated store to demonstrate query, show, stats, and JSON/CSV export.
- [ ] Inspect sync dry-run behavior and demonstrate import/deduplication only against isolated fixtures or an approved narrow source.
- [ ] Review annotation, post-session recording, dashboard integration, and optional judge costs/data exposure.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. Avoid default broad discovery of private trajectories;
inspect scope and fallback behavior first. Do not sync or annotate the live store,
invoke LLM judging, or install session hooks without approval. Finish with
repeatable examples or explicit blockers and a new journal entry recording the
decision. Keep unrelated conversation content out of durable reports.

## Reference

- [Package documentation](../gptme-contrib/packages/gptme-sessions/README.md)
