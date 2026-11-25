---
name: github
description: Work with GitHub repositories, branches, issues, pull requests, Actions workflows, and repository configuration.
---

# GitHub

1. Resolve the repository, current branch, intended base, permissions and whether the request is for source, PRs, or CI. Check the existing status and GitHub rules before mutation.
2. Make the smallest branch or workflow change. Follow existing CI conventions, scope Actions permissions, and keep secrets out of diffs and logs. Respect the requested PR and merge scope.
3. Verify the remote revision and PR or workflow identity after authorized changes. Inspect actual check results or record the missing access, run or approval.

Report the files changed, verification run, and any unavailable environment or access.

[Product documentation](https://docs.github.com/en/actions)
