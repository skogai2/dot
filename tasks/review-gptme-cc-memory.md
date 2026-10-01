---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-cc-memory with Skogix

Review the package behind `gptme cc-memory-extract`,
`gptme cc-memory-prompt-submit`, and `gptme cc-memory-stop-hook`, all listed by
`gptme --help` on 2026-10-02. These are related extraction and hook entry points,
not three independent packages. Installed does not mean validated or enabled.

## Walkthrough

- [ ] Inspect installed version, entry-point source, supported inputs, and current hook configuration without changing it.
- [ ] Explain typed memories, retention/retrieval scoring, and the extraction-to-injection lifecycle.
- [ ] Exercise extraction against a synthetic trajectory and isolated memory directory.
- [ ] Exercise prompt-submit and stop-hook behavior with synthetic hook payloads; verify output and written files.
- [ ] Compare this package with the existing cross-runtime memory tool/store and identify duplication or conflicts.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. Inspect hook source before invoking it; do not assume hooks
support `--help` or are side-effect-free. Do not install hooks, extract private
conversations, or write to live memory stores without approval. Use isolated
fixtures first. Finish with repeatable examples, observed results or explicit
blockers, and the decision recorded in a new journal entry.

## Reference

- [Package documentation](../gptme-contrib/packages/gptme-cc-memory/README.md)
