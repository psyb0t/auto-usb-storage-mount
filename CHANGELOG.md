# Changelog

All notable changes per release. Versions follow [semver](https://semver.org).

## v0.1.2 — 2026-08-01

CI infrastructure only. No change to the script itself.

- Added `.github/workflows/mirror-and-archive.yml`: every push mirrors the repo to GitLab and Codeberg, and pushes to the default branch or a tag are archived to the Wayback Machine, Software Heritage and archive.org. `pipeline.yml` keeps only the jobs that build and publish; anything that leaves the host lives in the file beside it.
- Pull requests are disabled on both mirrors. They are force-pushed from GitHub, so anything merged there would be destroyed by the next sync. Issues and forking stay enabled.
- Added `.github/workflows/issue-pull.yml`: every six hours, issues opened on either mirror are copied back into GitHub, and closing the original closes the copy. The scheduled run jitters to avoid hammering both mirrors when GitHub fires the account's crons together; a manual run does not.

## v0.1.1 — 2026-07-27

- Added a GitHub Actions CI status badge to the README.

## v0.1.0 — 2026-07-27

Add README status badges.

- Added self-hosted version and license badges (rendered as SVGs on the `badges` branch by the `create-badges` CI job, no third-party render service). Added a pipeline.yml running the badges job.
