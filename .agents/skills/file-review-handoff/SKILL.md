---
name: file-review-handoff
description: Review a target file against evidence-based pass/fail checks, identify its changes, and delegate specialist findings when warranted. Use when asked to audit, validate, improve, or sign off on a specific file with test results and a change summary.
---

# Review a file and hand off specialist findings

1. Resolve the exact file, the user's intent, and whether edits are authorized. Read the relevant project instructions, the file, and the baseline when available. In Git, inspect committed, staged, and unstaged changes as applicable. Save the initial file state so the final report can distinguish existing changes from work done during review. If there is no earlier revision, identify the baseline as the file at intake.
2. Define applicable checks before editing. Give each check an ID, expected result, and verification method. Use the file's normal consumer where possible. Examples include parsing JSON, resolving Markdown links, validating CSV headers and a known row, and running an existing code test or build. Add a behavior or content check specific to the user's request. Mark checks that cannot run as **BLOCKED** with the reason.
3. Run the checks and record actual evidence such as a command result, file section, or input/output pair. Mark each as **PASS**, **FAIL**, or **BLOCKED**. A mandatory check with no evidence stays blocked. If every mandatory check passes and there is no unresolved finding, report the result and close the task.
4. Fix ordinary in-scope defects when edits are authorized. For a finding or required judgment that calls for domain expertise, hand it to one relevant subagent when available. Provide the file and baseline, finding, check IDs, expected outputs, scope, edit permission, and completion condition. Assign one writer to the file at a time. Ask the specialist to return either a focused improvement with evidence or a pass with its rationale. If delegation is unavailable, run checks you can verify and flag the unresolved domain judgment. For review-only requests, request findings or a proposed patch.
5. Wait for the specialist's result. Compare its changes against the intake state and user scope, integrate authorized improvements, and rerun the same checks on the final file. Resolve follow-up issues within scope when possible. Stop when all mandatory checks pass, an unresolved check requires user input or access, or further changes would exceed scope.
6. Report the final file and overall verdict. **PASS** means all mandatory checks passed. **FAIL** means a mandatory check failed. **BLOCKED** means a mandatory check is unresolved and none are known to fail. Include the per-check evidence, changed sections or paths, and specialist disposition when applicable. State which changes were already present and which were made during review.

| Check | Expected | Actual evidence | Result |
| --- | --- | --- | --- |
| Example — Markdown links | All local links resolve | One missing target at its referenced path | FAIL |
