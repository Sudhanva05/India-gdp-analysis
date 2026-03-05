# India GDP Analysis & Forecasting

## Project Overview

This project performs **data analysis and time-series forecasting of India's GDP** using historical data from the World Bank.

The goal is to:

* Understand long-term GDP trends
* Analyze yearly growth patterns
* Build forecasting models to predict future GDP

The project demonstrates a **complete data science workflow** including data cleaning, exploratory analysis, and forecasting.

---

## Dataset Source

World Bank Open Data
Indicator: **GDP (current US$)**

Dataset:
https://data.worldbank.org/indicator/NY.GDP.MKTP.CD

The dataset contains annual GDP values for countries worldwide from **1960 onwards**.

---

## Methodology

### 1. Data Cleaning

Raw World Bank data contains metadata rows and wide-format year columns.

Steps performed:

* Skipped metadata rows
* Filtered dataset for **India**
* Converted wide format → long format using `pandas.melt()`
* Removed missing values
* Saved cleaned dataset

Notebook:

```
01_data_cleaning.ipynb
```

---

### 2. Exploratory Data Analysis

The cleaned dataset was analyzed to understand GDP trends.

Analysis includes:

* GDP growth visualization
* GDP growth rate calculation
* Economic trend observations

Notebook:

```
02_gdp_analysis.ipynb
```

Key insight:
India’s GDP shows **slow growth until the 1990s**, followed by **rapid acceleration after economic liberalization**.

---

### 3. Forecasting Models

Two forecasting approaches were implemented.

#### Linear Regression (Baseline Model)

A simple regression model was used to predict GDP based on year.

Model:

```
GDP ≈ a × Year + b
```

This provides a baseline forecast but underestimates growth due to GDP’s exponential trend.

---

#### Prophet Time-Series Model

Facebook Prophet was used for advanced forecasting.

Advantages:

* Handles non-linear growth
* Detects trend changes
* Provides prediction confidence intervals

Forecast horizon:
**10 years (2025–2035)**

Notebook:

```
03_gdp_forecasting.ipynb
```

---

## Results

Key observations:

* India's GDP grew from **~37 billion USD in 1960**
  to **~3.9 trillion USD in 2024**

* Major acceleration occurs after **economic reforms in 1991**

* Prophet forecasting suggests continued strong growth, potentially reaching **~5 trillion USD by the mid-2030s**

---

## Forecast Visualization

The Prophet model produces:

* Historical GDP trend
* Future GDP predictions
* Confidence intervals for uncertainty

This provides a more realistic forecast compared to simple regression.

---

## Project Structure

```
india-gdp-analysis
│
├── data
│   ├── raw
│   └── processed
│
├── 01_data_cleaning.ipynb
├── 02_gdp_analysis.ipynb
├── 03_gdp_forecasting.ipynb
│
└── README.md
```

---

## Tech Stack

Python
Pandas
NumPy
Matplotlib
Scikit-Learn
Prophet
Jupyter Notebook

---

## How to Run

Clone the repository:

```
git clone https://github.com/Sudhanva05/India-gdp-analysis.git
cd India-gdp-analysis
```

Install dependencies:

```
pip install pandas numpy matplotlib scikit-learn prophet
```

Run the notebooks in order:

1️⃣ `01_data_cleaning.ipynb`
2️⃣ `02_gdp_analysis.ipynb`
3️⃣ `03_gdp_forecasting.ipynb`

---

## Future Improvements

Possible extensions:

* Compare forecasting models (ARIMA vs Prophet)
* Add GDP per capita analysis
* Build interactive dashboards using Streamlit
* Compare India with other major economies

---

## Author

Sudhanva J Rao
Computer Science Student
