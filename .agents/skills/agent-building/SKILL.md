---
name: agent-building
description: Create, adapt, or review reusable Agent Skills for ChatGPT, Codex, and GitHub Copilot. Use when turning a guide or repeatable workflow into a SKILL.md, adding a cross-client skill, or documenting its tests and discovery.
---

# Build an agent skill

1. Read the source guide or workflow and existing project instructions. Identify when the new skill should trigger, the inputs it needs, the expected output, and an adjacent request it should leave to another workflow.
2. Choose a short action-oriented name. Create the skill under the existing canonical skill root, or under `.agents/skills/<name>/` for a new shared repository skill. Match the folder and the manifest `name`. Preserve the current source path and behavior where practical when editing an existing skill.
3. Set a specific `description` with both the capability and likely user requests. In the body, put steps in execution order and identify required inputs, checks, and failure behavior. Link optional examples or scripts relative to the manifest. Include a script only if it makes a repeatable or fragile step more reliable.
4. Keep the shared workflow usable as Markdown instructions. If a shell, connector, or MCP tool is useful, state the prerequisite and provide a fallback or report the specific blocker when that capability is essential.
5. Follow [client setup and smoke tests](references/client-setup.md) when preparing or verifying the result for a target client. Validate the manifest, linked files, and any executable resources. Exercise a representative prompt, a missing input or failure, and a closely related out-of-scope prompt.
6. Hand off the paths, usage example, verification results, and any untested client surfaces. A valid source directory and a successful client invocation are distinct results. Preserve the repo as the source of truth.
