# Country Portrayals on Wikipedia (Data & Society Seminar)

## Overview
This project analyzes whether Wikipedia portrays countries differently depending on development level (HDI tier) and whether this varies across language editions and page types.

**Research question:** Do developed and developing countries receive systematically different portrayals on Wikipedia?

## Repository structure
- `final_project_main.ipynb`  — main notebook (end-to-end pipeline)
- `data/` — input and intermediate datasets 
- `figs/` — generated plots (plots)
- `report/` — final report PDF

## Data pipeline (high level)
1. Select 60 countries (top/middle/bottom 20 by HDI).
2. Resolve Wikipedia pages in multiple languages using Wikidata QIDs + sitelinks.
3. Extract and clean sections (including lead).
4. Sample sections per page to control volume.
5. Label sections with frames (conflict/development/neutral) and topic using an LLM prompt.
6. Aggregate to country-level frame shares.
7. Estimate developing–developed gaps with bootstrap confidence intervals.

## Requirements
- Python 3.10+ 
- Packages: `pandas`, `numpy`, `matplotlib`, `requests`

### Windows (PowerShell)

```powershell
# from repo root
python -m venv .venv
.\.venv\Scripts\Activate.ps1

python -m pip install --upgrade pip
pip install -r requirements.txt

# run notebook
jupyter notebook final_project_main.ipynb

```

### macOS (Terminal)

```bash
# from repo root
python3 -m venv .venv
source .venv/bin/activate

python -m pip install --upgrade pip
pip install -r requirements.txt

# run notebook
jupyter notebook final_project_main.ipynb
```
