# Security policy

## Reporting a vulnerability or exposure

Do **not** open a public issue for a vulnerability, a suspected credential
exposure, or any security-sensitive finding.

Report it privately to the repository owner (Eli Halvorson) through the
contact route on the account profile, with:

- what was found and where (repo, path, commit) — **never the secret value
  itself**; a redacted prefix (first 4 characters) is enough to identify it;
- when it was first observed, with timestamps;
- whether it appears in git history or only in a working tree.

## Estate rules this policy enforces

- No credential values in files, logs, issues, PRs, or chat — ever. Agents
  use approved credential stores and name-only references.
- A suspected exposure is treated as live until disproven: the finding is
  recorded, the affected item is named for the owner, and rotation is the
  **owner's** action — agents never rotate, mint, or write credentials.
- Security settings that only an account/repo admin can change (branch
  protection, Dependabot, secret-scanning enforcement) are tracked as an
  owner checklist, not applied by agents.

## Supported versions

This is a private estate repository set; only the default branch of each
repository is supported. Fixes land there first.

*Stub authored 2026-11-23 as part of the estate template set
(`org/github-all-20261123/templates/`). Assisted-by: LLM [Muse],
agent-drafted.*
