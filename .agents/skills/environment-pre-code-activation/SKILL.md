---
name: environment-pre-code-activation
description: Prepare a coding environment before building a web app, API, Python analytics project, or full-stack app. Use when selecting a stack, scaffolding framework entry points, setting up dependency manifests or Python virtual environments, configuring VS Code and GitHub, or recording local and cloud project locations.
---

# Activate the development environment

1. Identify the project root, OS, whether this is a new or existing checkout, intended app type, and entry points. Read existing manifests, lockfiles, runtime pins, and repository instructions. Use [stack and dependency setup](references/stack-and-dependencies.md) to select a stack and directory layout. Preserve established conventions for existing projects.
2. Initialize or clone the repo into the designated SSD project root. For new projects propose `<SSD-root>/Developer/Projects/<project-slug>`. Verify the actual SSD mount before creating folders there. Check the existing Git root, remotes, branch, and worktree so setup uses the intended checkout.
3. Create or update the dependency manifest and minimally wire each selected framework to its entry files. Create or reuse the Python virtual environment for Python components. Install selected packages now when possible. If blocked, update the relevant manifest when the dependency constraint is known, then record the install command and blocker. Track undecided packages with their purpose in a README backlog or as comments in a requirements file. Keep JSON parseable and record which lockfiles still need updating.
4. Save a relative `<project-slug>.code-workspace` with extensions selected for the stack. Use [editor, connections, and storage](references/editor-connections-storage.md) to verify VS Code with GitHub, ChatGPT with GitHub, Codex in VS Code, and ChatGPT with Google Drive. Open the workspace and install recommended extensions when the intended device is reachable.
5. Record the SSD checkout, Google Drive folder and snapshot status, and GitHub repo in the README. Use a public-safe alias for sensitive paths, and keep the actual private path or URL in a user-local record. Verify each location independently.
6. Run a build, import, or health check for each configured component. Report the chosen stack, files updated, exact commands and outcomes, connection checks, and any pending items. Hand off database setup, data flow and traffic, and knowledge-base documentation to their own workflows.
