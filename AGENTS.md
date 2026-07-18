# AGENTS.md — legacy R examples

Conventions for this repository (modernized legacy projects).

## Layout

- `projects/<slug>/` — source of truth (`.Rmd`, `data/`, optional `R/`, `outputs/`)
- `docs/` — GitHub Pages HTML only (knit targets)
- Do not commit large generated caches; see `.gitignore`

## Quality bar

- Prefer modern tidyverse (`|>`), explicit seeds, and relative paths from the project directory
- Show all substantive code in rendered HTML (`code_folding: show`)
- Preserve author voice; fix bugs, obsolete APIs, and science errors
- Prefer CmdStanR / `rstanarm` diagnostics (R-hat, ESS, LOO) when Bayesian models appear

## Knit

From each project directory:

```bash
Rscript -e 'rmarkdown::render("profit_optimization.Rmd", output_dir = "../../docs")'
```
