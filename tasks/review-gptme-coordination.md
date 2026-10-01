---
created: 2026-10-02
priority: medium
state: new
tags: [gptme-contrib, package-review]
---

# Review gptme-coordination with Skogix

Walk through `gptme coordination`, listed by `gptme --help` on 2026-10-02.
Decide whether its SQLite work claims and messaging fit concurrent dot sessions.
Installed command discovery is not functional validation.

## Walkthrough

- [ ] Inspect installed version, CLI help, database defaults, and authentication/claim identity handling.
- [ ] Explain work claims, expiry, completion/reclaim semantics, and targeted/broadcast messages.
- [ ] Point `COORDINATION_DB` at a temporary database and simulate two agents competing for one claim.
- [ ] Demonstrate completion, claim status, and message/inbox behavior using synthetic identities.
- [ ] Inspect how workspace task selection and `gptodo ready --skip-claimed` integrate with the package.
- [ ] Record results, limitations, and Skogix's decision: use, defer, or skip; create follow-up tasks if needed.

## Boundaries and completion

Review interactively. Never claim, complete, expire, or message real work as part
of the test. Do not modify the live coordination database or expose claim secrets.
Finish with isolated demonstrations or explicit blockers and a new journal entry
recording the decision and repeatable commands.

## Reference

- [Package documentation](../gptme-contrib/packages/gptme-coordination/README.md)
