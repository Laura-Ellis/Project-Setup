# Data Sources

Data in this repo keeps each source's own terms; it is not covered by the code license.

| Source | Endpoint or file | Access date | Records | Terms |
|---|---|---|---|---|
| EXAMPLE: NIH RePORTER API | https://api.reporter.nih.gov/v2/projects/search | YYYY-MM-DD | n | Public U.S. government data |

## Folder rules

- `data/raw/`: untouched downloads; never edited by hand
- `data/processed/`: outputs of code in `src/` or `notebooks/`; reproducible from raw
- Large files stay out of git (see `.gitignore`); this file records how to rebuild them
