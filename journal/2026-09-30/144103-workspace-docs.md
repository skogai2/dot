# Clarify workspace documentation and fix broken links

The full pre-commit suite failed only on two references to a missing
`knowledge/portable-agent-apps.md` document. The references were present in
the initial workspace commit; no local history exists for the target file.

With Skogix's approval, removed the inherited domain-agent-app packaging
section rather than inventing a guide unrelated to this workspace's role.
Updated [README.md](../../README.md) and
[ARCHITECTURE.md](../../ARCHITECTURE.md) to describe dot as a base-environment
agent instance built from a reusable template. Preserved the shared-tooling,
task, journal, and forking guidance, and clarified that an org-shared layer
is optional and not configured here.

After initializing submodules at their pinned revisions, all hooks passed
with `prek run --all-files`, including markdown link validation. No runtime
configuration or agent behavior was changed.
