# CO2_emission_time_series_analysis
Forecasting CO₂ emission trends using ARIMA modeling and visual analytics in R.
# CO2 Emissions Time Series Analysis using ARIMA (R)

This project presents a time series analysis of global and Sri Lankan CO₂ emissions using the ARIMA model in **R**. The aim is to analyze historical trends, detect seasonality, and forecast future CO₂ emission levels.

---

## Project Objectives

- Analyze the **global trend** of CO₂ emissions over time.
- Focus on **Sri Lanka's CO₂ emissions**, modeling trends and making forecasts.
- Handle missing data and clean the dataset appropriately.
- Apply **ACF and PACF** plots to determine model parameters.
- Use **ARIMA modeling** to forecast future emissions.
- Visualize both actual and forecasted CO₂ values with confidence intervals.

---

## Tools & Libraries Used

- `R` (programming language)
- `tidyverse` – for data manipulation
- `forecast` – for ARIMA modeling and forecasting
- `tseries` – for time series tools and tests
- `corrplot` – for visualizing correlations
- `ggplot2` – for additional visualization

---

## Data Preprocessing

- The CO₂ emissions dataset used in this project is sourced from Our World in Data.
- Direct CSV link used:
  "https://raw.githubusercontent.com/owid/co2-data/master/owid-co2-data.csv"
- Handled missing values:
  - Numerical: replaced using median imputation.
  - Categorical: keep it as it is since there is only one categorical column and that is not much important for the analysis.
- Converted the dataset into a time series object using the `ts()` function.

---

## Time Series Analysis

### 1. **Global CO₂ Emissions**
- Grouped CO₂ emissions data by year.
- Converted it into a univariate time series.
- Plotted and analyzed trend patterns.
- Applied ACF and PACF plots to determine suitable ARIMA parameters.

### 2. **Sri Lankan CO₂ Emissions**
- Filtered dataset for Sri Lanka using country column.
- Created a time series of Sri Lankan CO₂ emissions.
- Modeled using ARIMA and forecasted for the next 10 years.

---

## Forecasting

Used the `auto.arima()` function for automatic model selection. Forecasted emissions with 80% and 95% confidence intervals using:

```r
forecast(model, h = 10)

---


CO2_Time_Series_Analysis/
├── co2_analysis.R         # Main R script
├── global_co2_plot.png    # Global CO₂ emission trends
├── sri_lanka_co2_plot.png # CO2 emission for Sri Lanka
├── acf_plot.png # acf plot 
├── pacf_plot.png # pacf plot 
├── forecast_global.png # Forecast results for entire world
├── forecast_sri_lanka.png # Forecast results for Sri Lanka
├── README.md              # This file

---
## Conclusion
-Global CO₂ emissions show a clear upward trend.

-Sri Lanka has a relatively smaller share, but from that we can recognize a decreasing pattern throughout the years

-ARIMA models effectively capture and forecast emission patterns.

-These insights can be valuable for environmental policy, climate planning, and sustainability research.


