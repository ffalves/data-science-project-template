# Data Science Project Template

A reusable, clean and portfolio-ready template for amazing Data Science projects.

> Start with structure.  
> Add thinking.  
> Then code with less chaos.

## 1. Project overview

This repository is a reusable template for amazing Data Science projects. It was created to help structure analytical, statistical and machine learning projects in a professional, reproducible and easy-to-review way.

The goal is:

> Start new DS projects faster, with a structure that already thinks about data, notebooks, reusable code, documentation, SQL, reports, tests and an optional app.

This template can be used for study projects, portfolio projects, technical assessments, interview preparation, synthetic case studies or real-world analytical cases.

It is intentionally focused on **Data Science** approaches.

---

## 2. What this template is good for

This template can support different types of DS projects, such as:

| Project type | Examples |
|---|---|
| Exploratory Data Analysis | Business diagnosis, customer behavior, operational analysis |
| Statistical Analysis | Hypothesis testing, confidence intervals, inference |
| Experimentation | A/B tests, treatment effects, guardrails, decision rules |
| Causal Inference | Difference-in-differences, matching, uplift analysis |
| Bayesian Analysis | Bayesian comparisons, posterior probabilities, uncertainty analysis |
| Time Series | Forecasting, seasonality, trend analysis |
| Machine Learning | Classification, regression, ranking, clustering |
| Deep Learning | Neural networks, tabular DL, image/text experiments when applicable |
| Business Analytics | Metric design, decision support, executive recommendations |

You can use it for frequentist, Bayesian, causal, time series, ML or DL projects.

---

## 3. Tech stack

This template uses a lightweight but professional Python Data Science stack.

The goal is to keep the project modern, reproducible and pleasant to work with — because Data Science is already hard enough without dependency chaos.

### Core tools

| Tool | Purpose |
|---|---|
| Python 3.14 | Main programming language |
| uv | Fast Python package, dependency and environment management |
| Jupyter Notebooks | Exploration, analysis and analytical storytelling |
| Git + GitHub | Version control and project sharing |
| SQL | Analytical transformations, feature logic and metric calculations |
| Makefile | Shortcuts for common project commands |

### Data Science libraries

| Library | Purpose |
|---|---|
| pandas | Data manipulation and tabular analysis |
| NumPy | Numerical computing |
| SciPy | Scientific and statistical computing |
| statsmodels | Statistical modeling and inference |
| scikit-learn | Machine Learning workflows |
| matplotlib | Static visualizations |
| Plotly | Interactive visualizations |
| Streamlit | Optional lightweight app or dashboard |

### Development and quality tools

| Tool | Purpose |
|---|---|
| pytest | Automated tests |
| Ruff | Linting and formatting |
| mypy | Static type checking |
| pandas-stubs | Type support for pandas |
| pre-commit | Run checks before commits |
| nbstripout | Remove notebook outputs before committing |

### Recommended dependency setup

```bash
uv add pandas numpy scipy statsmodels scikit-learn matplotlib plotly jupyter ipykernel python-dotenv streamlit
```

### Recommended development setup

```bash
uv add --dev pytest ruff mypy pandas-stubs pre-commit nbstripout
```

### Development dependencies explained

The `--dev` flag tells `uv` to add packages as development dependencies.

These tools are not part of the main analytical logic. They are used to test, lint, format, type-check and maintain the project with less chaos and more confidence.

| Tool | Why it is used |
|---|---|
| `pytest` | Runs automated tests for functions, metrics, data validation rules and modeling utilities. |
| `ruff` | Provides fast Python linting and formatting. It helps keep code clean, consistent and readable. |
| `mypy` | Performs static type checking. It helps catch type-related mistakes before runtime. |
| `pandas-stubs` | Adds type support for pandas, improving the experience when using `mypy` with DataFrames. |
| `pre-commit` | Runs automated checks before each Git commit, helping prevent low-quality code from entering the repository. |
| `nbstripout` | Removes notebook outputs and unnecessary metadata before committing notebooks, keeping Git history cleaner. |

Why this matters:

1. `pytest` helps protect important functions from silent bugs.
2. `ruff` keeps the code clean without needing several separate formatting and linting tools.
3. `mypy` helps catch type inconsistencies earlier.
4. `pre-commit` reduces the chance of committing messy code.
5. `nbstripout` prevents notebooks from becoming huge Git monsters.

Suggested commands:

```bash
uv run pytest
```

```bash
uv run ruff check .
```

```bash
uv run ruff format .
```

```bash
uv run mypy src
```

```bash
uv run pre-commit install
```

```bash
uv run pre-commit run --all-files
```

```bash
uv run nbstripout --install
```

Small tools. Less chaos. Better Data Science projects.

---

## 4. Repository structure

```text
data-science-project-template/
├── app
│   └── streamlit_app.py
├── data
│   ├── processed
│   ├── raw
│   └── sample
├── docs
│   ├── contributing.md
│   ├── data_dictionary.md
│   └── methodology.md
├── Makefile
├── notebooks
│   ├── 01_generate_synthetic_data.ipynb
│   ├── 02_data_preparation.ipynb
│   ├── 03_exploratory_data_analysis.ipynb
│   ├── 04_core_analysis.ipynb
│   ├── 05_model.ipynb
│   └── 06_executive_summary.ipynb
├── pyproject.toml
├── README.md
├── reports
│   ├── figures
│   └── final_report.md
├── sql
│   ├── 01_build_base_table.sql
│   ├── 02_create_features.sql
│   └── 03_calculate_metrics.sql
├── src
│   └── project_package
│       ├── __init__.py
│       ├── config.py
│       ├── data_cleaning.py
│       ├── data_generation.py
│       ├── data_loading.py
│       ├── data_validation.py
│       ├── evaluation.py
│       ├── features.py
│       ├── metrics.py
│       ├── modeling.py
│       ├── plots.py
│       └── statistical_analysis.py
├── tests
│   ├── test_data_generation.py
│   ├── test_data_validation.py
│   ├── test_features.py
│   ├── test_metrics.py
│   └── test_modeling.py
└── uv.lock
```

---

## 5. Folder and file guide

### `data/`

Stores project data.

```text
data/
├── raw/
├── processed/
└── sample/
```

| Folder | Purpose |
|---|---|
| `data/raw/` | Original data, synthetic or real, before cleaning |
| `data/processed/` | Cleaned and analysis-ready data |
| `data/sample/` | Small sample datasets that can be safely committed to GitHub |

Recommended principle:

> Keep large data out of Git. Keep small samples when they help someone understand the project.

---

### `docs/`

Stores supporting documentation.

```text
docs/
├── contributing.md
├── data_dictionary.md
└── methodology.md
```

| File | Purpose |
|---|---|
| `contributing.md` | Project conventions, commit patterns, notebook rules and development workflow |
| `data_dictionary.md` | Description of datasets, columns, types, meanings and assumptions |
| `methodology.md` | Explanation of analytical, statistical, ML or modeling approach |

The README is the main entry point.

The `docs/` folder is where the project gets more detailed.

---

### `notebooks/`

Stores the analytical workflow.

```text
notebooks/
├── 01_generate_synthetic_data.ipynb
├── 02_data_preparation.ipynb
├── 03_exploratory_data_analysis.ipynb
├── 04_core_analysis.ipynb
├── 05_model.ipynb
└── 06_executive_summary.ipynb
```

Recommended notebook flow:

| Notebook | Purpose |
|---|---|
| `01_generate_synthetic_data.ipynb` | Generate synthetic data when the project does not use real data |
| `02_data_preparation.ipynb` | Clean, transform and prepare data for analysis |
| `03_exploratory_data_analysis.ipynb` | Explore data quality, distributions, patterns and assumptions |
| `04_core_analysis.ipynb` | Run the main statistical, analytical or business analysis |
| `05_model.ipynb` | Train, evaluate or compare models, when applicable |
| `06_executive_summary.ipynb` | Produce final tables, charts and business-facing recommendations |

Important principle:

> Notebooks are for exploration and storytelling. Reusable logic should move to `src/`.

Avoid creating a notebook graveyard. Your future self will thank you.

---

### `src/`

Stores reusable Python code.

```text
src/
└── project_package/
    ├── __init__.py
    ├── config.py
    ├── data_cleaning.py
    ├── data_generation.py
    ├── data_loading.py
    ├── data_validation.py
    ├── evaluation.py
    ├── features.py
    ├── metrics.py
    ├── modeling.py
    ├── plots.py
    └── statistical_analysis.py
```

| File | Purpose |
|---|---|
| `config.py` | Central project parameters, paths, constants and assumptions |
| `data_generation.py` | Synthetic data generation functions |
| `data_loading.py` | Functions to load datasets |
| `data_cleaning.py` | Data cleaning and transformation helpers |
| `data_validation.py` | Data quality and validation checks |
| `features.py` | Feature engineering logic |
| `metrics.py` | Business, statistical or ML metrics |
| `statistical_analysis.py` | Statistical tests, intervals, inference and analytical methods |
| `modeling.py` | Model training or model pipeline functions |
| `evaluation.py` | Model, experiment or analysis evaluation logic |
| `plots.py` | Reusable visualization functions |

Recommended principle:

> If you copy and paste the same logic twice, it probably belongs in `src/`.

---

### `sql/`

Stores analytical SQL scripts.

```text
sql/
├── 01_build_base_table.sql
├── 02_create_features.sql
└── 03_calculate_metrics.sql
```

| File | Purpose |
|---|---|
| `01_build_base_table.sql` | Build the main analytical table |
| `02_create_features.sql` | Create features or intermediate analytical fields |
| `03_calculate_metrics.sql` | Calculate metrics, aggregations or business KPIs |

SQL is included because many Data Science projects live close to analytical databases, warehouses and lakehouses.

---

### `reports/`

Stores final outputs.

```text
reports/
├── figures/
└── final_report.md
```

| Path | Purpose |
|---|---|
| `reports/figures/` | Final charts and visual assets |
| `reports/final_report.md` | Final written case study or analysis report |

The final report should answer:

1. What problem did we analyze?
2. What data did we use?
3. What methodology did we apply?
4. What did we find?
5. What decision or recommendation follows from the analysis?
6. What are the limitations and next steps?

---

### `app/`

Stores an optional lightweight app.

```text
app/
└── streamlit_app.py
```

Use this when the project benefits from a simple interactive interface.

Examples:

- experiment result dashboard;
- model score explorer;
- forecast viewer;
- segmentation explorer;
- metric monitoring mockup;
- executive demo.

---

### `tests/`

Stores automated tests.

```text
tests/
├── test_data_generation.py
├── test_data_validation.py
├── test_features.py
├── test_metrics.py
└── test_modeling.py
```

Tests help make the project more reliable and professional.

Recommended things to test:

| Test file | What to test |
|---|---|
| `test_data_generation.py` | Synthetic data shape, columns, reproducibility and value ranges |
| `test_data_validation.py` | Data quality rules and validation logic |
| `test_features.py` | Feature engineering transformations |
| `test_metrics.py` | Metric formulas |
| `test_modeling.py` | Basic model pipeline behavior |

Testing does not need to be complex. Start with critical functions.

---

## 6. How to use this template

### Option 1 — Use as a GitHub template

If this repository is configured as a GitHub Template Repository:

1. Click **Use this template**.
2. Create a new repository.
3. Rename the project.
4. Clone the new repository.
5. Start adapting the README, docs, notebooks and source package.

### Option 2 — Clone manually

```bash
git clone git@github.com:<your-user>/data-science-project-template.git new-data-science-project
cd new-data-science-project
rm -rf .git
git init
```

Then rename the package:

```text
src/project_package/
```

to something specific, for example:

```text
src/customer_churn/
src/pricing_analysis/
src/forecasting_case/
src/experiment_analysis/
```

---

## 7. Environment setup

This project uses `uv` for Python dependency and environment management.

### Install dependencies

```bash
uv sync
```

### Add a new dependency

```bash
uv add package-name
```

### Add a development dependency

```bash
uv add --dev package-name
```

### Run Python scripts

```bash
uv run python path/to/script.py
```

### Run tests

```bash
uv run pytest
```

### Run linting

```bash
uv run ruff check .
```

### Run formatting

```bash
uv run ruff format .
```

### Run type checking

```bash
uv run mypy src
```

### Run the Streamlit app

```bash
uv run streamlit run app/streamlit_app.py
```

---

## 8. Python version

This template is currently configured for:

```text
Python 3.14
```

Python 3.14 is used as the default project version.

For some Data Science, Machine Learning or Deep Learning libraries, compatibility may depend on the package version and operating system.

If needed, adjust the Python version in:

```text
.python-version
pyproject.toml
```

For maximum compatibility in some ML/DL contexts, Python 3.12 or 3.13 may still be useful alternatives.

---

## 9. Recommended project workflow

A good Data Science project should move from business question to reproducible recommendation.

Suggested flow:

```text
1. Define the business or analytical question
2. Document the methodology
3. Generate, load or collect data
4. Validate data quality
5. Prepare the analytical dataset
6. Explore the data
7. Run the core analysis
8. Train models, if applicable
9. Evaluate results
10. Produce charts and tables
11. Write the final report
12. Add tests for critical logic
13. Clean the README
14. Commit like a diva professional
```

---

## 10. Project adaptation checklist

When creating a new project from this template, update:

- [ ] Project title
- [ ] Business problem
- [ ] Analytical question or hypothesis
- [ ] Data source or synthetic data assumptions
- [ ] Target variable, if applicable
- [ ] Main metrics
- [ ] Statistical or modeling approach
- [ ] Notebook names, if needed
- [ ] Python package name under `src/`
- [ ] SQL scripts
- [ ] Final report
- [ ] Streamlit app, if applicable
- [ ] Tests
- [ ] README status section

---

## 11. Commit convention

This project recommends Conventional Commits.

Format:

```text
<type>(optional scope): <short description>
```

Examples:

```text
chore(project): initialize data science template
docs(readme): describe project structure
feat(data): add synthetic data generator
feat(metrics): implement core metric functions
feat(modeling): add baseline model pipeline
test(metrics): add metric calculation tests
refactor(src): move notebook logic to reusable modules
docs(report): add final analysis report
```

Recommended types:

| Type | Use for |
|---|---|
| `feat` | New functionality |
| `fix` | Bug fix |
| `docs` | Documentation |
| `test` | Tests |
| `refactor` | Code restructuring |
| `chore` | Setup, maintenance or configuration |
| `style` | Formatting only |
| `ci` | CI/CD changes |

Recommended scopes:

| Scope | Use for |
|---|---|
| `project` | Project setup and structure |
| `readme` | README updates |
| `docs` | Supporting documentation |
| `data` | Data generation, loading or preparation |
| `features` | Feature engineering |
| `metrics` | Metric logic |
| `analysis` | Analytical or statistical analysis |
| `modeling` | Model training or modeling logic |
| `evaluation` | Evaluation logic |
| `plots` | Visualization utilities |
| `tests` | Automated tests |
| `app` | Streamlit app |
| `sql` | SQL scripts |
| `report` | Final report |

---

## 12. What good looks like

A strong project created from this template should be:

- reproducible;
- easy to navigate;
- documented;
- statistically or analytically sound;
- clear about assumptions;
- honest about limitations;
- useful for decision-making;
- readable by both technical and business audiences;
- not just a pile of notebooks pretending to be a project.

The goal is to build an analytical artifact that someone can review, trust and learn from.

---

## 13. Origin and attribution

This template was created as a reusable starting point for Data Science projects.

If this repository helped you start a project, organize your workflow, prepare a portfolio case, study better or reduce project setup chaos, attribution is appreciated.

You can mention the original repository like this:

```text
Project structure based on the Data Science Project Template by Fefe Alves.
```

Or, if you publish your project on GitHub:

```markdown
This project was initialized from the [Data Science Project Template](<https://github.com/ffalves/data-science-project-template>) by Fefe Alves.
```

Clone it, adapt it, improve it.

---

## 14. Current status

Template setup in progress.

Next improvements:

- [ ] Fill documentation files in `docs/`
- [ ] Configure `pyproject.toml`
- [ ] Add basic reusable functions in `src/`
- [ ] Add starter tests
- [ ] Add example Makefile commands
- [ ] Add optional Streamlit starter app
- [ ] Convert this repository into a GitHub Template Repository

---

## 15. License

Add a license if you plan to make this repository public.

For portfolio and study templates, common options are:

- MIT License;
- Apache License 2.0;
- no license, if you do not want to grant reuse rights yet.

---