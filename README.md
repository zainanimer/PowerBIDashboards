# Power BI Dashboards

A collection of Power BI dashboards built from public datasets, covering data cleaning, exploration, and visualization.

## Dashboards

| Dashboard | Description | Data Preparation |
|---|---|---|
| [World Cup Dashboard](dashboards/world-cup-dashboard.pbix) | Visualizes FIFA World Cup history and statistics | Reviewed/shaped in Power Query |
| [Titanic Visualisations](dashboards/titanic-visualisations.pbix) | Explores passenger demographics and survival patterns from the Titanic dataset | Cleaned in Jupyter Notebook (Python/pandas) |
| [Spotify Dashboard](dashboards/spotify-dashboard.pbix) | Explores music streaming/track data trends | Reviewed/shaped in Power Query |
| [Deaths & Causes Dashboard](dashboards/deaths-causes-dashboard.pbix) | Global death counts by cause, country, and year | Cleaned in Jupyter Notebook (Python/pandas) |
| [Cybersecurity Threats Dashboard](dashboards/cybersecurity-threats-dashboard.pbix) | Visualizes cybersecurity threat/incident data | Reviewed/shaped in Power Query |

## Data Preparation

Two workflows were used depending on the dataset:

**Cleaned with Python (Jupyter Notebook) before loading into Power BI:**
- **Titanic** — handled missing values in `Age`, `Cabin`, and `Embarked`, checked for duplicates, fixed data types, and ran exploratory analysis (distribution, survival by gender/class) before building the dashboard. Notebook: [`notebooks/Titanic_Dataset.ipynb`](notebooks/Titanic_Dataset.ipynb)
- **Deaths & Causes** — renamed and standardized columns, dropped irrelevant fields, filled missing values with the median, fixed data types, consolidated inconsistent region/country labels, and checked for whitespace and outliers. Notebook: [`notebooks/death_dataset.ipynb`](notebooks/death_dataset.ipynb)

**Reviewed and shaped directly in Power Query:**
- World Cup, Spotify, and Cybersecurity Threats dashboards were reviewed and transformed using Power BI's built-in Power Query editor (no external Python cleaning step).

## Repository Structure

```
power-bi-dashboards/
├── README.md
├── dashboards/
│   ├── world-cup-dashboard.pbix
│   ├── titanic-visualisations.pbix
│   ├── spotify-dashboard.pbix
│   ├── deaths-causes-dashboard.pbix
│   └── cybersecurity-threats-dashboard.pbix
├── notebooks/
│   ├── Titanic_Dataset.ipynb
│   └── death_dataset.ipynb
└── screenshots/
    ├── world-cup.png
    ├── titanic.png
    ├── spotify.png
    ├── deaths-causes.png
    └── cybersecurity.png
```

## How to View

1. Clone or download this repository.
2. Open any `.pbix` file in [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/desktop) (free).
3. For the Titanic and Deaths & Causes dashboards, the corresponding notebook in `notebooks/` shows the full data cleaning process.

## Tools Used

- **Power BI Desktop** — dashboard building and DAX
- **Power Query** — data review and transformation (World Cup, Spotify, Cybersecurity Threats)
- **Python (pandas, matplotlib, seaborn, scipy, statsmodels)** — data cleaning and exploratory analysis (Titanic, Deaths & Causes)
