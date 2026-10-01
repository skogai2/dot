---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-dashboard with Skogix

Walk through `gptme dashboard`, listed by `gptme --help` on 2026-10-02.
Review static HTML/JSON generation and optional live serving; neither is validated yet.

## Walkthrough

- [ ] Inspect installed version, CLI help, available extras, and output defaults.
- [ ] Explain which workspace content is collected and how static output differs from live APIs.
- [ ] Generate HTML and JSON from a small synthetic workspace into a temporary output directory; inspect both.
- [ ] Review exposure of journals, tasks, sessions, and services before considering a real workspace dashboard.
- [ ] If useful and available, demonstrate live serving on loopback only and stop the test server afterward.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. No public hosting, non-loopback binding, persistent service,
or live workspace export without approval. Do not change agent URLs or existing
output directories. Finish with repeatable examples or explicit blockers and a
new journal entry recording the decision.

## Reference

- [Package documentation](../gptme-contrib/packages/gptme-dashboard/README.md)
