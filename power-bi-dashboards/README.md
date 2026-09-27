# Power BI Portfolio

A collection of Power BI dashboards built from Kaggle datasets, covering data cleaning, exploration, and visualization.

## Dashboards

### 🌍 World Cup Dashboard
Visualizes FIFA World Cup history — historical goals by squad age, goal distribution by country, and club representation by nation.
*Data preparation: reviewed in Python (Jupyter) + shaped in Power Query*

![World Cup overview](screenshots/world-cup-1-overview.png)
![World Cup clubs by country](screenshots/world-cup-2-clubs.png)

📄 [`dashboards/world-cup-dashboard.pbix`](dashboards/world-cup-dashboard.pbix)

---

### 🚢 Titanic Visualisations
Explores passenger demographics and survival patterns — survival by class, embarkation port, age group, and family size.
*Data preparation: cleaned in Jupyter Notebook (Python/pandas)*

![Titanic overview](screenshots/titanic-1-overview.png)
![Titanic embarkation port](screenshots/titanic-2-embarkation.png)
![Titanic age group](screenshots/titanic-3-age-group.png)

📄 [`dashboards/titanic-visualisations.pbix`](dashboards/titanic-visualisations.pbix)

---

### 🎧 Spotify Dashboard
Explores music streaming trends — top artists by streams, streams by language and gender, and streams by country.
*Data preparation: cleaned in Jupyter Notebook (Python/pandas)*

![Spotify overview](screenshots/spotify-1-overview.png)
![Spotify by language and gender](screenshots/spotify-2-language-gender.png)
![Spotify by country](screenshots/spotify-3-country-map.png)

📄 [`dashboards/spotify-dashboard.pbix`](dashboards/spotify-dashboard.pbix)

---

### ☠️ Deaths & Causes Dashboard
Global death counts by cause, country, and year, with a country-level death burden map.
*Data preparation: cleaned in Jupyter Notebook (Python/pandas)*

![Deaths & Causes overview](screenshots/deaths-causes-1-overview.png)
![Deaths & Causes global map](screenshots/deaths-causes-2-global-map.png)

📄 [`dashboards/deaths-causes-dashboard.pbix`](dashboards/deaths-causes-dashboard.pbix)

---

### 🛡️ Cybersecurity Threats Dashboard
Global cybersecurity incidents (2015–2024) — financial loss by year, attack type distribution, and geographic breakdown.
*Data preparation: reviewed/shaped in Power Query*

![Cybersecurity overview](screenshots/cybersecurity-1-overview.png)
![Cybersecurity incidents by attack type](screenshots/cybersecurity-2-incidents.png)
![Cybersecurity global map](screenshots/cybersecurity-3-global-map.png)

📄 [`dashboards/cybersecurity-threats-dashboard.pbix`](dashboards/cybersecurity-threats-dashboard.pbix)

## Data Preparation

**Cleaned with Python (Jupyter Notebook) before loading into Power BI:**
- **Titanic** — handled missing values in `Age`, `Cabin`, and `Embarked`, checked for duplicates, fixed data types, and ran exploratory analysis (distribution, survival by gender/class). Notebook: [`notebooks/titanic-dataset.ipynb`](notebooks/titanic-dataset.ipynb)
- **Spotify** — checked for duplicates and missing values, filled missing stream counts (`Lead`, `Feature`, `Solo` streams) with the median. Notebook: [`notebooks/spotify.ipynb`](notebooks/spotify.ipynb)
- **Deaths & Causes** — renamed and standardized columns, dropped irrelevant fields, filled missing values with the median, fixed data types, consolidated inconsistent region/country labels, and checked for whitespace and outliers. Notebook: [`notebooks/death-dataset.ipynb`](notebooks/death-dataset.ipynb)
- **World Cup** — reviewed structure, nulls, and duplicates in Python as a first pass. Notebook: [`notebooks/world-cup-dataset.ipynb`](notebooks/world-cup-dataset.ipynb)

**Reviewed and shaped directly in Power Query:**
- The **Cybersecurity Threats** dashboard was reviewed and transformed using Power BI's built-in Power Query editor, with no separate Python cleaning step.

## Data Sources

All datasets are sourced from [Kaggle](https://www.kaggle.com). Links and licenses below (fill in per dataset):

| Dataset | Kaggle Link | License |
|---|---|---|
| World Cup | _add link_ | _add license_ |
| Titanic | _add link_ | _add license_ |
| Spotify | _add link_ | _add license_ |
| Deaths & Causes | _add link_ | _add license_ |
| Cybersecurity Threats | _add link_ | _add license_ |

## Repository Structure

```
power-bi-portfolio/
├── README.md
├── dashboards/
│   ├── world-cup-dashboard.pbix
│   ├── titanic-visualisations.pbix
│   ├── spotify-dashboard.pbix
│   ├── deaths-causes-dashboard.pbix
│   └── cybersecurity-threats-dashboard.pbix
├── notebooks/
│   ├── titanic-dataset.ipynb
│   ├── death-dataset.ipynb
│   ├── spotify.ipynb
│   └── world-cup-dataset.ipynb
├── data/
│   ├── raw/
│   │   ├── world-cup-dataset.csv
│   │   ├── titanic-train.csv
│   │   ├── titanic-test.csv
│   │   ├── spotify-dataset.csv
│   │   ├── number-of-deaths.csv
│   │   └── cybersecurity-threats-2015-2024.csv
│   └── cleaned/
│       ├── cleaned-titanic-dataset.csv
│       ├── cleaned-spotify-dataset.csv
│       └── cleaned-death-dataset.csv
└── screenshots/
    ├── world-cup-1-overview.png
    ├── world-cup-2-clubs.png
    ├── titanic-1-overview.png
    ├── titanic-2-embarkation.png
    ├── titanic-3-age-group.png
    ├── spotify-1-overview.png
    ├── spotify-2-language-gender.png
    ├── spotify-3-country-map.png
    ├── deaths-causes-1-overview.png
    ├── deaths-causes-2-global-map.png
    ├── cybersecurity-1-overview.png
    ├── cybersecurity-2-incidents.png
    └── cybersecurity-3-global-map.png
```

## How to View

1. Clone or download this repository.
2. Open any `.pbix` file in [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/desktop) (free).
3. For Titanic, Spotify, Deaths & Causes, and World Cup, the corresponding notebook in `notebooks/` shows the data review/cleaning process.

## Tools Used

- **Power BI Desktop** — dashboard building and DAX
- **Power Query** — data review and transformation (Cybersecurity Threats, and initial shaping for all dashboards)
- **Python (pandas, matplotlib, seaborn, scipy, statsmodels)** — data cleaning and exploratory analysis (Titanic, Spotify, Deaths & Causes, World Cup)
