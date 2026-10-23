# {{cookiecutter.project_name}}

{{cookiecutter.project_short_description}}

**Portfolio page:** {{cookiecutter.portfolio_url}}

## Question

One sentence a non-technical reader can follow.

## Executive summary

- Finding 1, stated as a decision or takeaway
- Finding 2
- Finding 3

## Data

Sources, years, and record counts. Full details: [`data/DATA_SOURCES.md`](data/DATA_SOURCES.md). Column definitions: [`data/data_dictionary.csv`](data/data_dictionary.csv).

## Method

Approach, with formulas and abbreviations defined.

## Results

Key charts with one-line captions. Interactive versions are on the portfolio page.

## AI workflow

Summary of how AI tools were used and checked. Full log: [`reports/ai_workflow_log.md`](reports/ai_workflow_log.md).

## Same skills, other domain

Link to a related project that applies these methods outside biomedical research.

## Quick start

```bash
python tasks.py create-venv
# Windows (PowerShell)
.venv\Scripts\Activate
# macOS / Linux
source .venv/bin/activate
python tasks.py install
python tasks.py jupyter
```

Full setup: [`PROJECT_SETUP.md`](PROJECT_SETUP.md)

## Repo structure

```
data/raw/         untouched downloads
data/processed/   reproducible outputs
notebooks/        analysis notebooks
src/              reusable code
reports/          figures, summaries, AI workflow log
config/           settings and colors
```

## License and citation

Code: MIT ([`LICENSE`](LICENSE)). Data: each source's own terms ([`data/DATA_SOURCES.md`](data/DATA_SOURCES.md)). To cite: [`CITATION.cff`](CITATION.cff).
