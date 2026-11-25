# Editor, connections, and storage

## Save the workspace

Create or update the project-root `<project-slug>.code-workspace`. Use `"folders": [{"path": "."}]` for a single project root. Keep personal interpreter paths and credentials out of shared settings. Open it with `code <project-slug>.code-workspace` when VS Code is available.

| Need | Workspace extension recommendation |
| --- | --- |
| Codex | `openai.chatgpt` |
| GitHub PRs and issues | `GitHub.vscode-pull-request-github` |
| React and TypeScript with ESLint | `dbaeumer.vscode-eslint` |
| Project configured for Prettier | `esbenp.prettier-vscode` |
| Python | `ms-python.python`, `ms-python.vscode-pylance` |
| Python notebooks | `ms-toolsai.jupyter` |

Install only the extensions relevant to the selected stack using VS Code or `code --install-extension <publisher.extension>`. Verify with `code --list-extensions`. A recommendation or installed extension alone does not verify sign-in.

## Verify the connections

| Connection | Evidence to record |
| --- | --- |
| VS Code ↔ GitHub | Open the SSD workspace. Confirm Source Control sees the repo, inspect `git remote -v` in its terminal, and read an authorized PR through the signed-in GitHub extension. |
| ChatGPT ↔ GitHub | Read a known file from the target repository through the connected capability on the intended ChatGPT surface. |
| Codex ↔ VS Code | Open the extension, complete the client’s sign-in if prompted, and ask it to identify a tracked file in the current workspace. |
| ChatGPT ↔ Google Drive | Find or list the intended Drive folder through the connected capability. |

## Record the three locations

Use the SSD as the active working copy, GitHub as versioned source, and Google Drive for approved source snapshots. Record the SSD checkout path or alias, GitHub URL, and Drive folder plus latest snapshot commit or pending status in the README. Keep secrets, dependency caches, virtual environments and active Git internals out of Drive copies. Confirm the SSD path and remote, the GitHub branch, and the actual file in Drive before recording the three locations as verified. Record each unavailable device or missing sign-in individually.

## References

- [VS Code extension recommendations](https://code.visualstudio.com/docs/configure/extensions/extension-marketplace)
- [GitHub in VS Code](https://code.visualstudio.com/docs/sourcecontrol/github)
- [Codex in VS Code](https://developers.openai.com/codex/ide/)
- [GitHub in ChatGPT](https://help.openai.com/en/articles/11145903-connecting-github-to-chatgpt)
- [Google Drive in ChatGPT](https://help.openai.com/en/articles/10929079-google-drive-app-and-setup-in-chatgpt)
