---
created: 2026-10-02
priority: medium
state: new
tags: [gptme, package-review, local-wrapper]
---

# Review the local gptme-web launcher with Skogix

`gptme web` appears in installed external commands in `gptme --help` on
2026-10-02, but is a local launcher rather than a gptme-contrib package.
Source inspection of `/home/skogix/.local/bin/gptme-web` showed that it starts
`gptme-server.service`, waits for loopback port 5700, reads the private token from
`/home/skogix/.config/gptme/server.env`, and opens the UI using `xdg-open`.
It was not executed during task creation.

## Walkthrough

- [ ] Inspect the current wrapper and user service definition without displaying secrets.
- [ ] Explain launcher behavior, authentication, readiness checks, and how the UI differs from the dashboard package.
- [ ] Check the existing service state and listening address without restarting it or disrupting other sessions.
- [ ] With approval, demonstrate the launcher and UI connection without logging or sharing the authenticated URL.
- [ ] Review failure diagnostics, startup behavior, and how to stop the service safely when no other session needs it.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. The inspected wrapper does not parse arguments: even
`gptme web --help` would start the service and open a browser. Read its source
instead of probing help blindly. Do not expose tokens, change service settings,
stop a shared server, or bind beyond loopback without approval. Finish with
observed behavior or explicit blockers and a new journal entry recording the
decision and safe repeatable steps.
