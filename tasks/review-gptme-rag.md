---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-rag with Skogix

Walk through `gptme rag`, listed by `gptme --help` on 2026-10-02.
Review this package's CLI and integration options, not just the in-session RAG tool.
Installed command discovery does not establish working embeddings or indexes.

## Walkthrough

- [ ] Inspect installed version, CLI help, optional dependencies, and index/cache defaults.
- [ ] Explain vector search, local versus remote embeddings, optional lexical retrieval, and MCP integration.
- [ ] Index a small synthetic corpus into an isolated persistence directory and cache using an approved backend.
- [ ] Search known concepts and identifiers; compare results with exact search and note failures or weak matches.
- [ ] Review watching, MCP serving, model downloads, resource costs, and relation to the in-session RAG tool.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. No whole-home indexing, live index mutations, remote
embedding calls, large model downloads, or persistent watchers without approval.
Reuse relevant evidence from the tool-validation task instead of duplicating it.
Finish with repeatable examples or explicit blockers and a new journal entry
recording the decision; missing dependencies are not successful validation.

## References

- [Package documentation](../gptme-contrib/packages/gptme-rag/README.md)
- [Inspection and retrieval tool validation](validate-tool-inspection-retrieval.md)
