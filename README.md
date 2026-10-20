# Open Food Facts Analysis

An exploratory analysis of an Open Food Facts product dataset, implemented in
[World_Food_Facts.ipynb](World_Food_Facts.ipynb).

The notebook explores missing data, product categories, nutrient distributions,
palm-oil and additive patterns, ingredient text, contribution dates, SQLite export,
and correlations with nutrition scores. Its saved analysis describes a historical
snapshot with 356,027 products and 163 columns; a newer export may have a different
schema and will not necessarily reproduce the saved results.

## Setup

Use a Python 3.10 environment. The saved notebook records Python 3.8.5;
`requirements.txt` supplies compatibility bounds for the older pandas and seaborn
APIs used here. These bounds are not a lockfile or an end-to-end reproduction.

```bash
git clone https://github.com/kamelch/open-food-facts-analysis.git
cd World_Food_Facts_Analysis
python -m pip install -r requirements.txt
python -m jupyterlab
```

Launch JupyterLab from the repository root and open `World_Food_Facts.ipynb`.

## Input data

The large source TSV is not included. Place a compatible historical Open Food Facts
export at `data/en.openfoodfacts.org.products.tsv` before running the import cell.
The notebook now reads from this repository-local location rather than a file in
the parent directory. Obtain the dataset under its own license; the repository's
MIT license covers the project code, not the external product database.

The analysis expects historical columns such as `pnns_groups_1`, `pnns_groups_2`,
`ingredients_from_palm_oil_n`, and `nutrition-score-fr_100g`. Review column names
before substituting a current export.

## Repository contents

- `World_Food_Facts.ipynb`: analysis and saved visualizations.
- `requirements.txt`: notebook dependency compatibility bounds.
- `data/`: local input data, excluded from Git apart from `.gitkeep`.
- `database_food_facts.sqlite`: local output created by the notebook, excluded from Git.

Saved notebook outputs remain available for review without the source data.
Changes to the notebook should explain their effect on the analysis and describe
which cells were rerun. See [CONTRIBUTING.md](CONTRIBUTING.md) for commit conventions.

## Repository purpose and workflow

Exploratory notebook covering product data quality, ingredients, additives, and nutrition-score patterns.

Canonical repository: https://github.com/kamelch/open-food-facts-analysis

See [CONTRIBUTING.md](CONTRIBUTING.md) for commit, branch, validation, and generated-file conventions.
