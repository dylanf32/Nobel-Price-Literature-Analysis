# Nobel Prize in Literature — Data Analysis

A collaborative notebook project that collects, prepares, and explores Nobel Literature laureate and author-work data, with geographic datasets for visualization.

**Stack:** Python · Pandas · NumPy · Jupyter  
**Dataset snapshot:** 2025, as documented in the original project notes.

## Start here

Open [report_notebook.ipynb](report_notebook.ipynb) in Jupyter or VS Code to explore the project report. Run notebooks from the repository root so relative `data/` paths resolve correctly. The report is large because it includes notebook content and outputs.

The repository does not include a dependency manifest. Pandas, NumPy, and Requests are used by the inspected collection/preparation notebooks; install additional visualization and geographic dependencies required by the report's import cells in your environment.

## Data sources

- [Wikipedia: Nobel laureates in Literature](https://en.wikipedia.org/wiki/List_of_Nobel_laureates_in_Literature)
- [Fantastic Fiction](https://www.fantasticfiction.com/) for novelist and works information
- Geographic shapefiles included under `data/`

The checked-in files let you inspect the existing snapshot without refreshing the source websites. Collection cells may be commented out to avoid repeated requests.

## Refresh workflow

Run the notebooks in this order:

| Order | Notebook | Purpose |
| --- | --- | --- |
| 1 | [wiki_data_collection.ipynb](wiki_data_collection.ipynb) | Collect laureate data |
| 2 | [wiki_data_preparation.ipynb](wiki_data_preparation.ipynb) | Prepare laureate and author fields |
| 3 | [works_data_collection.ipynb](works_data_collection.ipynb) | Collect works using the prepared author information |
| 4 | [works_data_preparation.ipynb](works_data_preparation.ipynb) | Prepare works datasets |
| 5 | [report_notebook.ipynb](report_notebook.ipynb) | Review the resulting analysis |

Website HTML can change, so review collection code before refreshing. Retain the collection notebook's request delays.

## Repository guide

| Path | Contents |
| --- | --- |
| `data/WinnersData.csv` | Collected laureate table |
| `data/laureates*.csv` | Laureate datasets |
| `data/*year_works.csv`, `data/total_works.csv` | Works summaries |
| `data/*.pkl` | Intermediate author data |
| `data/*shapefile/`, `data/geo_laureates/` | Geographic files |
| Root-level notebooks | Collection, preparation, and report workflows |

## Team

UCF Group 16:

| Contributor | Role |
| --- | --- |
| Thomas Tibbetts | Data cleaning |
| Sebastian Gonzalez Zurita | Analysis |
| Dylan Ferrer | Visualization |
| Bret Geyer | Presentation |

This is a group project; the repository includes contributions across collection, preparation, analysis, visualization, and presentation.
