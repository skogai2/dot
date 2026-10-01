---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-wisdom with Skogix

Walk through `gptme wisdom`, listed by `gptme --help` on 2026-10-02.
Review local BM25/SQLite FTS5 reference-text retrieval and optional prompt context.
The installed command has not yet been functionally validated.

## Walkthrough

- [ ] Inspect installed version, CLI help, database location, and source metadata requirements.
- [ ] Explain reference-book search versus semantic RAG and structural codegraph retrieval.
- [ ] Ingest a small synthetic reference text into an isolated database selected with `--db`.
- [ ] Demonstrate listing, relevant and no-match searches, source filtering, context output, and removal in that fixture database.
- [ ] Inspect generated context-command configuration without applying it; discuss licensed sources and useful books.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. Do not download books, modify the live index, or change
workspace prompt configuration without approval. Use only permitted source texts
and preserve attribution/license metadata. Finish with repeatable examples or
explicit blockers and a new journal entry recording the decision.

## Reference

- [Package documentation](../gptme-contrib/packages/gptme-wisdom/README.md)
