---
created: 2026-10-01
state: todo
priority: medium
tags: [tools, validation, documentation]
---

# Validate and demonstrate integrations and runtime helper tools

Demonstrate integration discovery and session helpers without publishing test
content, changing shared configuration, or polluting persistent memory.

## Scope

- `gh`: read-only GitHub repository, issue, PR, or workflow inspection.
- `mcp`: list loaded servers, inspect capabilities, and discover servers.
- `todo`: manage an isolated set of session-local test items.
- `memory`: document persistent memory usage; test writes only with approval.
- `vent`: document friction reporting; invoke only for a genuine blocker.
- `autocommit`: observe automatic commit hints when naturally triggered.
- `autocompact`: document automatic context compaction and observe if triggered.

## Procedure

- [ ] Inspect current tool availability and invocation signatures.
- [ ] Record which tools are explicitly callable versus automatic runtime hooks.
- [ ] Use gh to inspect a public repository and a relevant issue or PR, including comments.
- [ ] Compare returned identifiers and fields with the requested GitHub object.
- [ ] List currently loaded MCP servers and inspect one if available.
- [ ] Demonstrate MCP discovery without installing or starting a server.
- [ ] Read the current todo list before adding uniquely named test items.
- [ ] Add, rename, transition, and remove only the test todo items; verify unrelated items survive.
- [ ] Document memory invocation and its persistence scope; request approval before any write.
- [ ] If approved, save a genuinely useful preference or fact and verify through an available read path.
- [ ] Document vent usage without submitting a fabricated friction report.
- [ ] Observe automatic hook behavior where feasible; otherwise record it as not exercised.
- [ ] Record actual invocations, expected and observed results, and cleanup.

## Safety boundaries

GitHub checks are read-only. Do not create comments, issues, PRs, commits,
workflow dispatches, or merges merely to demonstrate an integration.

Do not load, install, or start MCP servers without approval. Server startup
executes code; discovery and metadata inspection are distinct from permission
to run it. Do not expose credentials or private resource contents in reports.

Do not clear existing todos. Persistent memory tests must not insert invented
preferences or disposable facts that future sessions might treat as true.
Do not fabricate frustration to exercise vent. Do not force context exhaustion
or create unnecessary commits to trigger automatic hooks.

If authentication, network access, or a safe target is missing, record that
specific limitation rather than silently substituting a different tool.

## Success criteria

Each scoped capability has one of: verified, failed, blocked, or not exercised,
with supporting evidence and an explanation. Documentation-only examples are
clearly distinguished from observed tool execution.

Write results to `knowledge/tool-validation/integrations-runtime.md` and append
a new dated journal entry. Include a concise usage example for each capability,
redacting private identifiers and secrets. Mark done when the demonstrations
and report are complete, preserving untested coverage explicitly.

## Related

- [Task lifecycle](../TASKS.md)
- [Inspection validation](validate-tool-inspection-retrieval.md)
- [Editing validation](validate-tool-file-data-editing.md)
- [Execution validation](validate-tool-execution-visuals.md)
