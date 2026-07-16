# Git Workflow — Operating Procedure

Standard procedure for working across repositories and devices in a cloud-first setup. Applies to every repository cloned locally — the Knowledge Operating System repository and any project-specific public repository alike.

This describes *how* work moves between devices via GitHub. For how content itself moves through editorial stages within a repository, see the root [WORKFLOW.md](../WORKFLOW.md) — a different document, a different question.

## The three rules

1. **Pull at the start of every working session.**
   `git pull` — before making any change, bring the local clone up to date with GitHub.
2. **Push at the end of every working session.**
   `git push` — before closing the laptop or switching devices, send every commit to GitHub.
3. **Verify the working tree is clean before finishing.**
   `git status` should report "nothing to commit, working tree clean" before a session ends. If it doesn't, either commit the change or explicitly decide it isn't ready yet — don't leave uncommitted work stranded on one device.

## Why

GitHub, not any single laptop, is the source of truth. A clone left behind on one device with unpushed commits is invisible everywhere else — these three rules keep every device's copy equivalent to what's on GitHub.
