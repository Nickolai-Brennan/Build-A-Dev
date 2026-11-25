# Building skills for ChatGPT, Codex, and GitHub Copilot

Build-A-Dev keeps one source directory per skill. Start with the [Agent Building Skill](.agents/skills/agent-building/SKILL.md) to turn a repeatable task into a skill and verify it with example requests.

## Author a skill

1. Write a representative request, the required inputs, and what a successful result looks like. Include a request close enough to test whether the skill triggers too broadly.
2. Name the folder and the manifest identically. Use lowercase letters, digits, and single hyphens between words. The [Agent Skills specification](https://agentskills.io/specification) limits names to 64 characters and descriptions to 1,024 characters.
3. Put discovery cues in the description. Keep the workflow in the body and link to scripts, fixture data, or detailed references only when they help execute the task.
4. Use flexible guidance where several approaches work. Specify exact steps where order, permissions, or the output contract matters.
5. Test a realistic request, a missing input or failure, and the nearby out-of-scope request. Record what the client actually loaded and ran.

```markdown
---
name: summarize-api-usage
description: Summarize request volume and error rates from API logs. Use when asked to compare API usage or failures over a time window.
---

# Summarize API usage

1. Identify the log source, time window, and status-code field.
2. Count requests and calculate error rates with the request count as the denominator.
3. Report source coverage and return a table by endpoint. If there are no requests, report an undefined rate.
```

## Load the same source in each client

| Client | Use | Verify |
| --- | --- | --- |
| ChatGPT | Open **Skills → Create → Upload from your computer** where enabled. Upload the individual skill with its supporting files using a format the uploader accepts. For an instruction-only skill, the editor is also an option. | Confirm the skill is available after review, invoke it in a chat, and check that any linked resource is usable. |
| Codex | Open the checked-out repo. Codex local clients discover repo-level `.agents/skills/<skill-name>/SKILL.md`. | Select the skill or mention it explicitly, then run a realistic request. |
| GitHub Copilot | Use the same `.agents/skills/<skill-name>/SKILL.md` on a supported Copilot surface. Copilot also accepts `.github/skills`, so use that path only if a target setup requires it. | Open the branch that contains the change and confirm Copilot uses the workflow. |

Keep `name` and `description` in the shared frontmatter. Use relative paths inside the package. Treat optional client metadata as an extension only when the target needs it. A skill can describe tool use. Configuring MCP and granting tool permissions happen separately in the client.

## Review and handoff

- Link to the exact skill source and its supporting files.
- Check discovery, execution, fallback behavior, and output in each target client you can access. Record untested clients explicitly.
- Keep each reusable instruction in one source. Include only dependencies or resources needed to complete the workflow.

## References

- [Original skill authoring reference](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)
- [Skills in ChatGPT](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)
- [Build skills for ChatGPT and Codex](https://learn.chatgpt.com/docs/build-skills)
- [Add agent skills to GitHub Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills)
