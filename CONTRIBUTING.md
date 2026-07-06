# Contributing

Thanks for your interest in tpt-solutions projects. This organization runs on
an **issues-only** contribution model.

## How to contribute

- **Found a bug or have a feature idea?** Open an issue using the
  [bug report](.github/ISSUE_TEMPLATE/bug_report.yml) or
  [feature request](.github/ISSUE_TEMPLATE/feature_request.yml) form on the
  relevant repository.
- **We do not accept unsolicited pull requests.** The maintainer (with AI
  assistance) implements all fixes and features directly. Pull requests
  opened by outside contributors will be closed and redirected to an issue.
  This keeps review overhead low for a solo-maintained set of projects.
- Please search existing issues before opening a new one to avoid duplicates.
- Be as specific as possible: steps to reproduce, expected vs. actual
  behavior, environment details, and logs/screenshots where relevant.

## Repository standards (for reference)

Every code repository in this organization follows the same conventions:

- **Build tool:** a `justfile` at the repo root exposing at least:
  - `just lint`
  - `just test`
  - `just build`
  - `just dev`
- **CI:** a thin `.github/workflows/ci.yml` that calls this repo's reusable
  workflow for the project's language, e.g.:

  ```yaml
  name: CI
  on: [push, pull_request]
  jobs:
    ci:
      uses: tpt-solutions/.github/.github/workflows/ci-rust.yml@main
      # or ci-go.yml / ci-node.yml
  ```

- **Labels:** synced from the canonical [`labels.yml`](labels.yml) in this
  repo via the reusable
  [`label-sync.yml`](.github/workflows/label-sync.yml) workflow.
- **Stale issues:** each repo schedules the reusable
  [`stale.yml`](.github/workflows/stale.yml) workflow, e.g.:

  ```yaml
  name: Stale
  on:
    schedule:
      - cron: "0 0 * * *"
  jobs:
    stale:
      uses: tpt-solutions/.github/.github/workflows/stale.yml@main
  ```

- **Topics:** each repo should carry topics for its primary language,
  `tpt-solutions`, and a category tag (e.g. `cli`, `library`, `service`). Set
  these under repo Settings → Topics, or with
  `gh repo edit --add-topic <topic>`.

## Code of Conduct

This project follows the [Code of Conduct](CODE_OF_CONDUCT.md). By
participating, you're expected to uphold it.

## Security issues

Do not open a public issue for security vulnerabilities — see
[SECURITY.md](SECURITY.md).
