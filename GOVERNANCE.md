# Governance

This organization is solo-maintained (with AI assistance), not run by a
committee or foundation. This document sets expectations for how it works.

## How work gets prioritized

There is no formal RFC process. The [issues-only contribution
model](CONTRIBUTING.md) is the only intake path: bug reports and feature
requests come in as issues, and the maintainer decides what to work on next.
Roughly, in order:

1. Security issues (see [SECURITY.md](SECURITY.md))
2. Bugs affecting the current release
3. Everything else, at the maintainer's discretion

## Response times

There is no SLA. Issues are triaged as time allows. The `status:
needs-triage`, `status: in-progress`, and `priority: *` labels reflect
current state — an issue without a priority label simply hasn't been
looked at yet, not rejected.

## Stale issues

Issues with no activity are automatically marked stale and eventually closed
by the stale-bot workflow (60 days to stale, 14 more to close — see
[CONTRIBUTING.md](CONTRIBUTING.md)). This is the mechanism for keeping the
issue tracker current; it's not a judgment on the issue's merit. Add a
comment or the `pinned` label to keep something open longer.

## Getting help

For questions rather than bug reports, see [SUPPORT.md](SUPPORT.md)
(Discord and issue guidance).
