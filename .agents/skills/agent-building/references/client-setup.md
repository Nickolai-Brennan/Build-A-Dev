# Client setup and smoke tests

| Target | Setup | What to exercise |
| --- | --- | --- |
| ChatGPT | In a workspace where Skills upload is available, go to **Skills → Create → Upload from your computer**, include all supporting files, and wait for the review status. | Invoke in a fresh chat and confirm the workflow can access any required resource or uses the documented fallback. |
| Codex | Launch a local Codex client in the checked-out repo containing `.agents/skills/<name>/SKILL.md`. | Select or mention the skill, then try a fresh request whose wording matches the description. |
| GitHub Copilot | Open the checkout or branch with the same `.agents/skills` path in a supported surface such as VS Code agent mode or Copilot CLI. | Confirm discovery and run the same request from a fresh session. |

## Source checks

- Use the public Agent Skills specification for the naming and frontmatter contract.
- Resolve every relative reference from the file that contains it and include the target in the package.
- Run added scripts with safe fixture inputs where executable tools are available.
- Record the client, version or surface when available, prompt, observed response, and outcome. Mark surfaces you cannot run as untested.

## Official docs

- [Agent Skills specification](https://agentskills.io/specification)
- [ChatGPT Skills](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)
- [ChatGPT and Codex skill authoring](https://learn.chatgpt.com/docs/build-skills)
- [Copilot agent skills](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills)
