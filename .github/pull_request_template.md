<!--
Estate PR contract (workspace AGENTS.md): agents are contributors, never
approvers. An agent opens this PR; a human understands and defends every
changed line before it merges. Agents never merge — including their own PRs.
-->

## What

<!-- What changed, in plain terms. Link the issue/ticket this answers:
     Linear id, certification item, programme register, or ledger entry.
     No orphan work. -->

## Why

<!-- The problem or ruling this answers, with the evidence that it exists. -->

## Evidence

<!-- Test commands run + exit codes + pass/fail counts, re-run at delivery
     time (never quoted from an earlier log). Probe/read-back output for
     state changes, with timestamps. Bug fixes: the reproducer and the
     regression test named for the bug, failing before / passing after. -->

## What was NOT done

<!-- Required. Checks skipped, surfaces untouched, known gaps. Silence is
     not coverage. -->

## Rails checklist

- [ ] No merge by an agent — this PR waits for a human merge
- [ ] No credentials, tokens, or secrets in any file, log, or comment
- [ ] No force-push, no history rewrite, no direct commit to `main`/`master`
- [ ] Spend: $0, or the spend is named here with its per-item approval
- [ ] Green claims are timestamped and re-verified, not carried forward
- [ ] Zero new lint/type warnings on touched files

Assisted-by: LLM [Muse] · agent-drafted
