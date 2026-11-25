# Stack and dependency setup

| Project | Evidence | Example starting layout |
| --- | --- | --- |
| React frontend | JS manifest, lockfile, Vite config | `package.json`, `index.html`, `src/main.tsx`, `src/App.tsx` |
| Python API | Python manifest, ASGI entry point | `requirements.txt` or `pyproject.toml`, `app/main.py`, `tests/` |
| Python analytics | Python manifest, scripts or notebooks | Python manifest, `src/`, `tests/`, `notebooks/` when used |
| Full-stack | Separate app manifests or workspace config | `frontend/` and `backend/` unless the repository already has a layout |
| Tooling-only or another stack | README, existing manifests and CI | Follow the project’s runtime and avoid adding an unused manifest |

## Node and React

Use the existing package manager. For npm, use `npm ci` with an in-sync lockfile and `npm install` when resolving or intentionally updating dependencies. For a new React SPA, use the official scaffold in an empty target and record the selected Node version.

```bash
npm create vite@latest frontend -- --template react-ts
cd frontend
npm install
npm run build
```

Check that the HTML root matches the React mount, the imports resolve, and the package scripts run. Install `@tanstack/react-query` if the selected feature needs remote-state caching or `@tanstack/react-table` if it needs data-table behavior. Where React Query is chosen, wire its provider at the app root and verify one query. Put known blocked dependencies under `dependencies` or `devDependencies` in valid `package.json`. Keep unknown versions or undecided packages in a README backlog. In full-stack projects, check a frontend request reaches the backend via the configured development proxy or API origin.

## Python

Use the repository’s existing dependency workflow. For pip-based projects, declare selected packages in `requirements.txt`. For a pyproject-based workflow, retain its `pyproject.toml` and lock/sync process. Record the Python version, ignore `.venv/` in Git, and select that environment as the VS Code interpreter.

```bash
# POSIX. Run from the Python component directory.
python3 -m venv .venv
.venv/bin/python -m pip install -r requirements.txt
.venv/bin/python -m pip check
```

```powershell
# Windows PowerShell. Run from the Python component directory.
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m pip check
```

Select pandas only when the work needs tabular analytics. Verify its import and a tiny calculation when installed. A deferred requirement can be a comment such as `# pandas — add a version constraint when tabular analytics is selected`. For a Python API, verify the framework import and a minimal health endpoint. Report build or import status, manifest and lock status, and how to retry blocked installs.

## References

- [Vite guide](https://vite.dev/guide/)
- [npm ci](https://docs.npmjs.com/cli/v11/commands/npm-ci/)
- [Python venv](https://docs.python.org/3/library/venv.html)
