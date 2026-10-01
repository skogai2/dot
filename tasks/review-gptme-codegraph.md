---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-codegraph with Skogix

Review `gptme codegraph`, `gptme codegraph-commit-map`, and
`gptme codegraph-mcp` together. All three appear in `gptme --help` on 2026-10-02;
functionality and optional extras remain unvalidated.

## Walkthrough

- [ ] Inspect installed version, CLI signatures, tree-sitter support, and MCP dependencies.
- [ ] Explain structural retrieval versus exact search and semantic RAG.
- [ ] Use a tiny multi-file fixture to demonstrate symbols, definitions, callers/callees, and dependency blast versus change impact.
- [ ] Generate a repo map in the fixture, check freshness, change a source, and verify stale detection without making a Git commit.
- [ ] Inspect the MCP entry point and demonstrate an isolated request if its dependencies are available.
- [ ] Record accuracy limits, examples, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. Keep indexes and generated maps inside the fixture; do not
add hooks, MCP configuration, or generated artifacts to real projects without
approval. Stop any test server after the demonstration. Finish when all entry
points have observed results or explicit blockers and a new journal entry records
the decision and repeatable commands.

## Reference

- [Package documentation](../gptme-contrib/packages/gptme-codegraph/README.md)
