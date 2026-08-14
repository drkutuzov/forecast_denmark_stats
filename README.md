# Forecasting Danish Statistics

Time-series analysis and forecasting of publicly available Danish statistical data using **R**.

This repository explores statistical forecasting methods on real-world data from **Statistics Denmark (Danmarks Statistik)**. The project covers data preparation, exploratory time-series analysis, decomposition, model fitting, forecast evaluation, and visualization across several economic and production datasets.

## Overview

The purpose of this repository is to demonstrate a practical workflow for forecasting Danish statistical time series.

The analyses include:

* exploratory time-series analysis and visualization
* identification of trends and seasonal patterns
* seasonal decomposition
* training and test set separation
* fitting statistical forecasting models
* out-of-sample forecast evaluation
* comparison of forecasting accuracy
* residual diagnostics
* visualization of forecasts and prediction intervals

Forecast performance is evaluated using standard metrics such as **MAE**, **RMSE**, **MAPE**, **MASE**, and **Theil's U**, together with residual autocorrelation diagnostics.

## Data

The analyses use publicly available statistical data from **Statistics Denmark (Danmarks Statistik)** and its StatBank.

Statistics Denmark provides programmatic access to published StatBank data through its public API.

Data source: **Statistics Denmark — StatBank**

The datasets in this repository represent examples from different domains, allowing forecasting methods to be tested on time series with different trends, seasonal structures, and noise characteristics.

## Forecasting examples

The repository currently contains the following analyses:

| Notebook                                  | Forecasting problem                    |
| ----------------------------------------- | -------------------------------------- |
| `danish_cars_forecast.ipynb`              | Danish car statistics                  |
| `danish_butter_production_forecast.ipynb` | Butter production in Denmark           |
| `danish_cheese_production_forecast.ipynb` | Cheese production in Denmark           |
| `danish_milk_fat_forecast.ipynb`          | Milk-fat related production statistics |
| `danish_pe_ratio_forecast.ipynb`          | Danish P/E ratio time series           |

Each notebook provides an independent example of applying time-series methods to Danish statistical data.

## Repository structure

```text
forecast_denmark_stats/
│
├── data/
│
├── danish_butter_production_forecast.ipynb
├── danish_cars_forecast.ipynb
├── danish_cheese_production_forecast.ipynb
├── danish_milk_fat_forecast.ipynb
├── danish_pe_ratio_forecast.ipynb
├── LICENSE
└── README.md
```

## Requirements

The analyses are written in **R** and presented as Jupyter notebooks.

To run the notebooks, you need:

* R
* Jupyter Notebook or JupyterLab
* an R Jupyter kernel (`IRkernel`)
* the R packages imported by the individual notebooks

To install the R kernel for Jupyter:

```r
install.packages("IRkernel")
IRkernel::installspec()
```

After cloning the repository, start Jupyter from the project directory and open one of the notebooks.

## Clone the repository

```bash
git clone https://github.com/drkutuzov/forecast_denmark_stats.git
cd forecast_denmark_stats
```

Then start Jupyter:

```bash
jupyter notebook
```

or:

```bash
jupyter lab
```

## Motivation

Official statistical databases provide a large collection of structured, regularly updated time series describing economic activity, production, demographics, transportation, and other aspects of society.

These datasets provide a useful environment for studying forecasting because they contain many of the challenges encountered in real-world time-series modelling, including:

* long-term trends
* seasonal variation
* changing variance
* autocorrelation
* structural changes
* limited historical observations

This repository uses Danish public statistics as practical examples for developing, comparing, and evaluating statistical forecasting approaches.

## Data source and attribution

The statistical data originate from **Statistics Denmark (Danmarks Statistik)**.

When using or redistributing the underlying data, please follow the attribution and licensing requirements specified by Statistics Denmark.

## License

The source code in this repository is available under the **MIT License**. See `LICENSE` for details.
