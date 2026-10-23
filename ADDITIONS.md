# Template additions for Project-Setup

Copy these into the Project-Setup repo after unarchiving it, then tick Settings > Template repository.

| File | Where it goes | Change |
|---|---|---|
| `cookiecutter.json` | repo root | Replaces current file; adds author name parts, ORCID, portfolio URL, and year |
| `{{cookiecutter.project_slug}}/README.md` | project template folder | Replaces generated README; keep your TL;DR wording if you prefer it in Quick start |
| `{{cookiecutter.project_slug}}/LICENSE` | project template folder | New: MIT |
| `{{cookiecutter.project_slug}}/CITATION.cff` | project template folder | New: citation metadata |
| `{{cookiecutter.project_slug}}/data/data_dictionary.csv` | project template folder | New: column definitions, one example row |
| `{{cookiecutter.project_slug}}/data/DATA_SOURCES.md` | project template folder | New: sources, access dates, terms |
| `{{cookiecutter.project_slug}}/reports/ai_workflow_log.md` | project template folder | New: prompt log and validation checklist |

Also add to the repo root README: macOS/Linux activation (`source .venv/bin/activate`).

Test after copying:

```bash
pip install cookiecutter
cookiecutter path/to/Project-Setup --no-input project_name="Test Project"
```
