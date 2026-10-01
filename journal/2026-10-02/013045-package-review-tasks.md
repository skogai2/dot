# Queue installed external-command walkthroughs

Skogix requested individual tasks to review installed gptme-contrib packages
visible in `gptme --help`, together one at a time.

Inspected the actual help output and package script declarations/documentation.
Created nine new review tasks covering all 13 listed external commands, grouping
multiple entry points from the same package:

- [Activity summary](../../tasks/review-gptme-activity-summary.md)
- [Claude Code memory](../../tasks/review-gptme-cc-memory.md): extract, prompt-submit, stop-hook
- [Codegraph](../../tasks/review-gptme-codegraph.md): CLI, commit-map, MCP
- [Coordination](../../tasks/review-gptme-coordination.md)
- [Dashboard](../../tasks/review-gptme-dashboard.md)
- [RAG](../../tasks/review-gptme-rag.md)
- [Sessions](../../tasks/review-gptme-sessions.md)
- [Wisdom](../../tasks/review-gptme-wisdom.md)
- [Web launcher](../../tasks/review-gptme-web.md)

The web command is a local wrapper, not a contrib package. Source inspection
showed that it starts the server and opens an authenticated browser URL even if
passed `--help`; the task warns against blindly invoking it. No token was read
and the wrapper was not executed.

Each task includes a package-specific walkthrough, isolated demonstrations,
safety boundaries, and a use/defer/skip decision with Skogix. All remain new;
no walkthroughs or configuration changes were performed. Packages not exposed
in the observed external-command list are outside this batch.

Validation: `gptodo check` accepted all 14 workspace tasks, including the nine
new ones. Package functionality has not been validated by creating these tasks.
