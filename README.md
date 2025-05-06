# Global CO₂ Emissions – Exploratory Analysis & Visualisation

A data‑driven exploration of historical and contemporary carbon‑dioxide emissions across countries, built around the **Our World in Data CO₂ and Greenhouse Gas Emissions** dataset.

---

## 🌍 Project Overview

This notebook walks through an end‑to‑end workflow:

1. **Ingest & Clean** the OWID dataset (1960 → present).
2. **Engineer Features** such as cumulative emissions, emissions intensity, fossil‑fuel decomposition, and low‑carbon energy share.
3. **Exploratory Data Analysis (EDA)** to answer policy‑relevant questions, illustrated with clear Matplotlib/Seaborn visuals.
4. **Machine‑Learning Teaser** – a lightweight XGBoost model to estimate a country’s total CO₂ output from macro‑economic and energy‑mix variables.

The goal is to provide a concise yet extensible foundation for climate‑data storytelling or further modelling work.

---

## 🔍 Guiding Questions

* **Top Emitters Today vs. 1990** – who leads in absolute terms and how has the ranking shifted?
* **Emissions Intensity** – is CO₂ per‑unit‑GDP falling faster in developed or developing economies?
* **GDP ↔︎ CO₂ Relationship** – how tightly are wealth and emissions still coupled?
* **Success Stories** – which countries have reduced gross emissions since 1990?
* **Energy Mix** – what share of each nation’s consumption is low‑carbon?
* **Regional Comparisons** – distributions of per‑capita emissions within geographic blocs.
* **Cumulative vs. Current Emissions** – historic responsibility vs. present‑day output.

These questions are laid out as headings inside `co2_analysis.ipynb` and can be tweaked or expanded.

---

## 📂 Repository Structure

```
.
├── data/
│   └── owid-co2-data.csv      # Raw dataset (~15 MB, 60k rows)
├── figures/                   # Auto‑saved plots & images
├── co2_analysis.ipynb         # Main notebook (you’re here)
├── environment.yml            # Conda spec (alternative to requirements.txt)
├── requirements.txt           # Python package list
└── README.md                  # Project documentation (this file)
```

> **Tip:** Keep `data/` out of version control with a `.gitignore` entry or use Git LFS if you must track the CSV.

---

## ⚙️ Quick Start

### 1. Clone + Set Up

```bash
# Clone the repo
$ git clone https://github.com/your‑username/co2‑analysis.git
$ cd co2‑analysis

# Create a Python 3.9 virtualenv (pip)
$ python -m venv .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
```

*or* with Conda:

```bash
$ conda env create -f environment.yml
$ conda activate co2‑analysis
```

### 2. Get the Data

```bash
$ mkdir -p data
$ curl -L -o data/owid-co2-data.csv \
  https://github.com/owid/co2-data/raw/master/owid-co2-data.csv
```

### 3. Run the Notebook

```bash
$ jupyter lab  # or jupyter notebook / VS Code
```

Open `co2_analysis.ipynb`, run cells from top to bottom, and explore the outputs & plots.

---

## 🖥️ Dependencies

| Package    | Tested Version |
| ---------- | -------------- |
| Python     | 3.9            |
| pandas     | ≥ 2.2          |
| numpy      | ≥ 1.26         |
| matplotlib | ≥ 3.8          |
| seaborn    | ≥ 0.13         |
| xgboost    | ≥ 2.0          |
| tqdm       | ≥ 4.66         |

Install via `pip install -r requirements.txt` or let Conda handle exact versions.

---

## 📊 Key Outputs

* Time‑series plots of the **top 10 emitters** (absolute & per‑capita).
* Heat‑map correlation matrix between GDP, population, energy metrics and emissions.
* Histogram of **per‑capita CO₂** with log‑scaled long tail.
* Regional boxplots contrasting **G7, BRICS, and Least‑Developed Countries**.
* Bar‑chart ranking of countries that **cut emissions since 1990**.
* Feature‑importance chart from the XGBoost demo.

All figures are automatically saved to `figures/` when the notebook is executed.

---

## 🚧 Extending the Project

* Swap in methane or nitrous‑oxide columns for a broader GHG study.
* Build interactive dashboards with Plotly/Dash or Streamlit.
* Train forecasting models (ARIMA, Prophet, LSTM) on per‑country time series.
* Deploy a lightweight API to serve model predictions.

Feel free to open a PR or issue with ideas!

---

## 📜 License & Attribution

* Code – MIT License (see `LICENSE`).
* Data – © Our World in Data, licensed under Creative Commons BY 4.0.
  Please cite *Hannah Ritchie and Max Roser (2024) – “CO₂ and Greenhouse Gas Emissions”.*  See OWID for full terms.

---

## 🙏 Acknowledgements

* **Our World in Data** for maintaining the open CO₂ dataset.
* **Climate Action Tracker** & **IEA** for methodological inspiration.

---

### 📮 Questions?

Ping me via GitHub Issues or email – happy to chat!
