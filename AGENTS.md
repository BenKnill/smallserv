# Operating mode
You are the sole implementer. Do not ask me to write code. Produce changes ONLY via GitHub pull requests (PRs).

# Ground rules
- Treat main as the single source of truth. I do NOT care about preserving old code. Replacements and deletions are allowed.
- Create one PR at a time. Do not open a new PR until the previous one is merged.
- Keep history linear. Use squash merge only.

# Branching + sync procedure (mandatory)
1) Before every task:
   - git fetch --prune
   - git switch -c feature/<short-task>-<UTC-yyyymmdd-HHMM> origin/main
2) Generate code by replacing full files/directories you “own” rather than patching lines.
3) Before pushing:
   - git fetch --prune
   - git rebase origin/main  # If conflicts appear, prefer YOUR newly generated content; recreate files as needed.
   - If rebase conflicts: `git rebase --abort`, delete the conflicted files, regenerate them from scratch, and re-run the rebase.
4) Push branch and open a PR with "squash" as the merge method. Enable auto-merge.
5) Enqueue the PR in the Merge Queue if available. Do not attempt manual merging.
6) After merge completes, delete the feature branch locally and remotely.

# Conflict-avoidance rules
- Never edit the same area across concurrent PRs. Since you control PR creation, serialize them.
- Prefer file replacement over surgical edits. You may delete obsolete files.
- If main changes beneath you, re-run step (3). Do NOT force-push to main; only update your feature branch.

# PR hygiene
- PRs should be self-contained and rerunnable: re-creating the repo from main + your PR must yield identical results.
- PR title: “[codex] <task summary>”
- PR body: Brief what/why; note that older code may be removed intentionally.
