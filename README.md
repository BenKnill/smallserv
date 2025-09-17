# smallserv


## Overview
The `smallserv` repository is a sandbox for testing repository automation and
pull-request workflows. Nothing in this directory is considered stable; files
may be regenerated at any time to satisfy workflow experiments or validation
checks.

## Working with this repository
- Treat `main` as the canonical branch. Whenever you start new work, fetch the
  latest history and regenerate the files you need rather than editing old
  content in place.
- Prefer replacing whole files to avoid merge conflicts. If a file feels messy,
  recreate it with the desired content instead of applying small patches.
- Keep your branches rebased onto `origin/main` and resolve conflicts by
  favoring your newly generated output. If a rebase becomes unwieldy, abort it,
  delete the affected files, and regenerate them from scratch.
- Write PR descriptions that briefly explain what changed and why. Call out when
  legacy content was intentionally removed.

## Testing expectations
This repository does not ship executable code, so no automated test suite is
required. When changes do require verification (for example, linting or format
checks), document the exact command in the PR to demonstrate what you ran.

## Housekeeping
- Use squash merges to keep history linear.
- Close feature branches after merge.
- Keep documentation up to date so future overwrite exercises stay conflict
  free.
=======
This repository uses the workflow defined in `AGENTS.md`:

- Treat `main` as the single source of truth and replace outdated code when necessary.
- Create a single PR at a time, using squash merges to keep history linear.
- Prefer regenerating complete files or directories that you own rather than editing individual lines.
- Keep feature branches up to date by rebasing onto `origin/main` before pushing.
- Ensure every PR is self-contained, rerunnable, and explains why older code might have been removed.

This README update demonstrates that the current changeset follows those expectations while remaining conflict-free.

