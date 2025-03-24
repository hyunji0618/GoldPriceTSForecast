# Gold Price Forecasting Using Time Series Modeling

📎 **[View Presentation Slides (PDF)](https://github.com/hyunji0618/GoldPriceTSForecast/blob/main/Gallagher_Gold%20Price%20Prediction.pdf)**

## Project Overview
This project focuses on predicting global gold prices using a range of time series forecasting techniques including LSTM, MLP (Neural Network), ARIMA, ETS, and Prophet. We analyzed historical gold price data and relevant macroeconomic indicators—such as the S&P 500, crude oil prices, and the US Dollar Index—to develop models that accurately forecast future gold price movements.

## Authors
- **Amy Kim**
- **Cicily Mathew**
- **Olivia Rumere**

## Institution
- **Course:** Time Series Analysis and Forecasting
- **Instructor:** Fan Yang
- **University:** University of Chicago
- **Date:** March 11th, 2025

## Table of Contents
- [Introduction](#introduction)
- [Data Collection](#data-collection)
- [Methodology](#methodology)
- [Results](#results)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Presentation](#presentation)

## Introduction
Gold prices are influenced by various factors including economic indicators, geopolitical events, and market sentiment. Accurate forecasting of gold prices is valuable to investors, policymakers, and analysts. This project applies both statistical and deep learning-based time series models to forecast gold prices and evaluate the impact of macroeconomic factors on prediction performance.

## Data Collection
The dataset was collected from Yahoo Finance using the `yFinance` API. It includes:

- **Gold Price** (USD/oz)
- **Crude Oil Price** (USD/barrel)
- **US Dollar Index**
- **S&P 500 Index**

**Time Span:** January 2, 2014 – February 28, 2025 (11 years, 2804 daily observations)  

The data collection process is documented in the Jupyter Notebook: `Gallagher_GoldPrice_Data_Collection_from_YFinance.ipynb`.

## Methodology
We implemented and compared the following models:

- **ARIMA**
- **ETS (Exponential Smoothing)**
- **Prophet**
- **MLP (Multi-layer Perceptron)**
- **LSTM (Long Short-Term Memory)**

### Process:
1. **Exploratory Data Analysis**: Trends, seasonality, stationarity, ACF/PACF plots, and correlation heatmaps.
2. **Data Preprocessing**: Missing value handling, log transformation, differencing, normalization.
3. **Feature Engineering**: Incorporation of macroeconomic indicators.
4. **Model Training & Evaluation**: Models trained on training/test splits; evaluated using RMSE (Root Mean Square Error) and MAE (Mean Absolute Error).

### Notebooks:
Detailed analyses and results are available in the following notebooks:
- `Gallagher_Gold_Price_Only_Prediction.ipynb` – Gold price only models  
- `Gallagher_Gold_Price_with_Macroeconomic_Variables.ipynb` – Models trained with macroeconomic features (S&P 500, Oil Crude prices, and the US Dollar Index)

## Results
- The **LSTM model** with log-transformed gold prices and S&P 500 as a feature achieved the **best performance** (RMSE = 0.028).
- Incorporating **macroeconomic indicators significantly improved** model accuracy across all models.
- Deep learning methods like **LSTM outperformed traditional models**, especially when handling complex temporal dependencies.

For more details, refer to the project documentation and presentation slides.

## Usage
1. Clone or extract the repository.
2. Install required dependencies using `pip install -r requirements.txt`.
3. Open Jupyter Notebook and navigate to the project directory.
4. Execute the notebooks in the following order:
   - `Gallagher_GoldPrice_Data_Collection_from_YFinance.ipynb`: Retrieves and merged the gold price and macroeconomics data from Yahoo Finance.
   - `Gallagher_Gold_Price_Only_Prediction.ipynb`: Data Preprocessing, Exploratory Data Analysis, and Model Development using Gold Price Only Data to Predict Gold Price
   - `Gallagher_Gold_Price_with_Macroeconomic_Variables.ipynb`: Analysis and Model Development using Gold Price and Macroeconomic Variables to Predict Gold Price

## Dependencies
- Python 3.8+
- Pandas
- NumPy
- Matplotlib
- Seaborn
- TensorFlow/Keras (for LSTM models)
- Scikit-learn
- Statsmodels (for ARIMA and ETS models)
- Prophet (Facebook’s forecasting model)
- yFinance (for data retrieval)

Install dependencies using:
```
pip install -r requirements.txt
```
