# HOMELLC Assignment - Data Cleaning, Analysis, and Model Training Pipeline

Find publicly available data for key factors that influence US home prices nationally. Then, build a data science model that explains how these factors impacted home prices over the last 20 years.Use the S&P Case-Schiller Home Price Index as a proxy for home prices: fred.stlouisfed.org/series/CSUSHPISA

This repository contains Jupyter Notebooks designed for cleaning, exploring, and analyzing data, as well as training machine learning models. The workflow is split into three main stages, each represented by a dedicated notebook.

## Notebooks

### 1. **Data Cleaning**

- **File:** `cleaning_data.ipynb`
- **Purpose:**
  - Prepares raw datasets for analysis and modeling.
  - Ensures the data is clean and formatted for subsequent analysis.

### 2. **Data Exploration and Analysis**

- **File:** `explore_data.ipynb`
- **Purpose:**
  - Performs exploratory data analysis (EDA) to uncover insights.
  - Handles missing values, outliers, and data transformations.
  - Visualizes key trends and distributions within the data.
  - Summarizes relationships and patterns to guide modeling decisions.

### 3. **Model Training**

- **File:** `model.ipynb`
- **Purpose:**

  - Trains machine learning models on the processed data.
  - Evaluates model performance and generates predictions.

  ---

## Feature Engineering

- `DATE`:

  - Dates for the past 20 Years.
- `CS_INDEX`:

  - Case-Schiller Home Price Index.
- `COST`:

  - Construction material cost.
  - Rising costs can limit housing supply, indirectly impacting prices.
- `EMP_TO_POP_RATIO`:

  - Employment to population ratio.
- `Per_Capita_GDP`:

  - Indicates the economic health and wealth of a population, influencing overall housing demand.
- `INFLATION`:

  - Inflation can affect housing affordability and construction costs.
- `INTEREST_RATES`:

  - Strongly impact housing affordability and borrowing costs, directly influencing demand.
  - Easily measurable and historically correlated with housing prices.
- `MONTHLY_SUPPLY`:

  - A direct measure of supply in the housing market, critical for understanding price dynamics.
- `PI`:

  - Reflects the purchasing power of population based on personal income and their ability to afford homes.
- `TOTAL_POPULATION`:

  - Total population.
- `UNEMPLOYMENT_RATE`:

  - High unemployment reduces demand, making this a crucial economic indicator for housing markets.

# Findings

1. What Matters Most:

   * The feature `COST (Construction material cost)` is the most important factor affecting the `CS_INDEX`. When `COST` goes up, the `CS_INDEX` also increases significantly.
2. Other Influences:

   * Factors like `EMP_TO_POP_RATIO`, `Per_Capita_GDP` and `INTEREST_RATES` also play a positive role but are less impactful compared to COST.
3. Negative Impact:

   * `INFLATION` (how much prices are rising) has a strong negative effect on the `CS_INDEX`. Higher inflation lowers the index.

   (Other features dont affect the `CS_INDEX`)

# Sources

1. CASE-SCHILLER Home Price Index - [https://fred.stlouisfed.org/series/CSUSHPISA](https://fred.stlouisfed.org/series/CSUSHPISA)
2. Construction Material Cost - [https://fred.stlouisfed.org/series/WPUSI012011](https://fred.stlouisfed.org/series/WPUSI012011)
3. Employment to Population Ratio - [https://fred.stlouisfed.org/series/EMRATIO](https://fred.stlouisfed.org/series/EMRATIO)
4. Per Capita GDP - [https://fred.stlouisfed.org/series/A939RX0Q048SBEA](https://fred.stlouisfed.org/series/A939RX0Q048SBEA)
5. Inflation - [https://fred.stlouisfed.org/series/WPUSI012011](https://fred.stlouisfed.org/series/WPUSI012011)
6. Interest rates - [https://fred.stlouisfed.org/series/FEDFUNDS](https://fred.stlouisfed.org/series/FEDFUNDS)
7. Monthly Supply of New Houses - [https://fred.stlouisfed.org/series/MSACSR](https://fred.stlouisfed.org/series/MSACSR)
8. Personal Income (PI) - [https://fred.stlouisfed.org/series/PI]([https://fred.stlouisfed.org/series/PI]())
9. Unemployment rate - [https://fred.stlouisfed.org/series/UNRATE](https://fred.stlouisfed.org/series/UNRATE)
10. Total households - [https://fred.stlouisfed.org/series/TTLHH](https://fred.stlouisfed.org/series/TTLHH)
11. Total Population - [https://fred.stlouisfed.org/series/POPTOTUSA647NWDB](https://fred.stlouisfed.org/series/POPTOTUSA647NWDB)

### References/Knowledge gaining

* [https://www.investopedia.com/articles/mortgages-real-estate/10/understanding-case-shiller-index.asp](https://www.investopedia.com/articles/mortgages-real-estate/10/understanding-case-shiller-index.asp)
* [https://www.investopedia.com/articles/mortages-real-estate/11/factors-affecting-real-estate-market.asp](https://www.investopedia.com/articles/mortages-real-estate/11/factors-affecting-real-estate-market.asp)
