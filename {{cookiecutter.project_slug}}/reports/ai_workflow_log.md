# AI Workflow Log

How AI coding assistants and LLMs were used in this project, and how their output was checked.

| Date | Task | Tool | Prompt (short) | What it got wrong | How I validated |
|---|---|---|---|---|---|
| YYYY-MM-DD | EXAMPLE: write API pagination loop | Claude | "Paginate RePORTER search, 500 per page" | Off-by-one on offset; missed last page | Compared record count to RePORTER web total |

## Validation checklist

- [ ] Row counts match the source
- [ ] Spot-checked 10 records by hand
- [ ] Summary statistics recomputed independently
- [ ] Generated SQL or code reviewed line by line before use
- [ ] LLM labels compared with a hand-coded sample (report agreement, e.g. Cohen's kappa)
