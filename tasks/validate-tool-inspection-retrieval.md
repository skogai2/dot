---
created: 2026-10-01
priority: medium
state: active
tags:
- tools
- validation
- documentation
---

# Validate and demonstrate workspace inspection and retrieval tools

Test read-only inspection and retrieval against small, known fixtures.
Demonstrate actual tool invocations, not just commands someone could run.

## Scope

- `shell`: working directory, Git status, file reads, and exact search with `rg`.
- `chats`: list sessions, search a known topic, and read a matching conversation.
- `rag`: index a dedicated fixture directory, search semantically, and inspect status.
- `lessons`: list and search existing guidance without modifying it.

## Procedure

- [ ] Inspect current tool availability and invocation signatures.
- [ ] Create a temporary fixture directory with known text and record its absolute path.
- [ ] Demonstrate shell inspection and exact search, including a no-match result.
- [ ] Exercise chats against this tool-testing topic; keep unrelated private conversation content out of durable reports.
- [ ] Index only the fixture directory with RAG, using an isolated project/index when supported.
- [ ] Compare a semantic search result with the known fixture content.
- [ ] Demonstrate lessons discovery and identify one relevant existing lesson.
- [ ] Record invocations, expected results, actual results, and limitations.

## Safety boundaries

Do not index the whole home directory, upload private files, or alter existing
indexes. If RAG needs a remote provider, credentials, or a shared index mutation,
pause that check for approval. Never treat an empty search as a tool failure
without checking whether a matching record exists.

## Success criteria

Each scoped tool has an observed result or a specific unavailable/blocked status.
The report includes a repeatable inspection/search example and distinguishes
exact search from semantic retrieval. Missing capabilities are not passes.

Write results to `knowledge/tool-validation/inspection-retrieval.md` and append
a new dated journal entry. Mark done when the demonstrations and report are
complete; preserve unresolved limitations explicitly.

## Related

- [Task lifecycle](../TASKS.md)
- [Editing validation](validate-tool-file-data-editing.md)
- [Execution validation](validate-tool-execution-visuals.md)
- [Integration validation](validate-tool-integrations-runtime.md)
