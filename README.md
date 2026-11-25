# Build-A-Dev

Reusable skills and development workflows for ChatGPT, Codex, and GitHub Copilot.

| Skill | Use it to |
| --- | --- |
| [Agent Building](.agents/skills/agent-building/SKILL.md) | Create or adapt a portable skill and verify its behavior. |
| [API Contracts](.agents/skills/api-contracts/SKILL.md) | Design a typed HTTP API and wire a frontend to it. |
| [MCP Tool Design](.agents/skills/mcp-tool-design/SKILL.md) | Define a tool for a backend capability and test its calls. |

Read [Building Skills 101](building-skills-101.md) for authoring and client setup.

## Product specialists

Load the specialist for the product named in the task. For cross-product work, use the specialist that owns each change and verify the integrated result. Use Data Visualization for metric and chart decisions, then use the named chart or dashboard tool's specialist for its integration.

| Specialist | Skill source | Evaluation cases |
| --- | --- | --- |
| React | [SKILL.md](.agents/skills/react/SKILL.md) | [Eval cases](.agents/skills/react/evals/evals.json) |
| Python | [SKILL.md](.agents/skills/python/SKILL.md) | [Eval cases](.agents/skills/python/evals/evals.json) |
| FastAPI | [SKILL.md](.agents/skills/fastapi/SKILL.md) | [Eval cases](.agents/skills/fastapi/evals/evals.json) |
| PostgreSQL | [SKILL.md](.agents/skills/postgresql/SKILL.md) | [Eval cases](.agents/skills/postgresql/evals/evals.json) |
| Obsidian | [SKILL.md](.agents/skills/obsidian/SKILL.md) | [Eval cases](.agents/skills/obsidian/evals/evals.json) |
| Vercel | [SKILL.md](.agents/skills/vercel/SKILL.md) | [Eval cases](.agents/skills/vercel/evals/evals.json) |
| AuthZed / SpiceDB | [SKILL.md](.agents/skills/authzed/SKILL.md) | [Eval cases](.agents/skills/authzed/evals/evals.json) |
| Neo4j | [SKILL.md](.agents/skills/neo4j/SKILL.md) | [Eval cases](.agents/skills/neo4j/evals/evals.json) |
| Storybook | [SKILL.md](.agents/skills/storybook/SKILL.md) | [Eval cases](.agents/skills/storybook/evals/evals.json) |
| Embeddable Developer Toolkit | [SKILL.md](.agents/skills/embeddable/SKILL.md) | [Eval cases](.agents/skills/embeddable/evals/evals.json) |
| ApexCharts | [SKILL.md](.agents/skills/apexcharts/SKILL.md) | [Eval cases](.agents/skills/apexcharts/evals/evals.json) |
| RAWGraphs | [SKILL.md](.agents/skills/rawgraphs/SKILL.md) | [Eval cases](.agents/skills/rawgraphs/evals/evals.json) |
| Syncfusion Essential Studio | [SKILL.md](.agents/skills/syncfusion-essential-studio/SKILL.md) | [Eval cases](.agents/skills/syncfusion-essential-studio/evals/evals.json) |
| Taipy | [SKILL.md](.agents/skills/taipy/SKILL.md) | [Eval cases](.agents/skills/taipy/evals/evals.json) |
| GitHub | [SKILL.md](.agents/skills/github/SKILL.md) | [Eval cases](.agents/skills/github/evals/evals.json) |
| NodeboxJS / Sandpack | [SKILL.md](.agents/skills/nodeboxjs/SKILL.md) | [Eval cases](.agents/skills/nodeboxjs/evals/evals.json) |
| Canva | [SKILL.md](.agents/skills/canva/SKILL.md) | [Eval cases](.agents/skills/canva/evals/evals.json) |
| Data Visualization Project | [SKILL.md](.agents/skills/data-visualization/SKILL.md) | [Eval cases](.agents/skills/data-visualization/evals/evals.json) |

Use the [skill evaluation guide](assets/docs/library/evaluating-skill-quality.md) to run a specialist and a baseline on the same prompt, then record pass/fail evidence.
