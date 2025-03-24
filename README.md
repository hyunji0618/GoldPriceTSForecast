# Gold Price Forecasting Using Time Series Modeling

## Project Overview
This project focuses on predicting global gold prices by employing time series forecasting techniques including LSTM, MLP(NN), ARIMA, ETS, and Prophet model. Through the analysis of historical gold price data and leveraging relevant macroeconomic indicators (S&P 500, Oil Crude prices, and the US Dollar Index), the project aims to build accurate models that can forecast future gold price movements.

## Authors
- **Amy Kim**
- **Cicily Mathew**
- **Olivia Rumere**

## Institution
- **Course:** Time Series Analysis and Forecasting
- **Instructor:** Fan Yang
- **University:** University of Chicago
- **Date:** March 11, 2025

## Table of Contents
- [Introduction](#introduction)
- [Data Collection](#data-collection)
- [Methodology](#methodology)
- [Results](#results)
- [Usage](#usage)

## Introduction
Gold prices are influenced by various factors, including economic indicators, geopolitical events, and market dynamics. Accurate forecasting of gold prices is valuable for investors, policymakers, and financial analysts. This project utilizes historical data and advanced time series modeling techniques to predict future gold prices.

## Data Collection
The dataset used in this project is sourced from Yahoo Finance, encompassing historical gold prices along with relevant macroeconomic indicators: 
- **Gold Price**: The target variable, measured in USD per ounce.
- **Oil Crude**: Crude oil prices in USD per barrel.
- **US Dollar Index**: Measures the strength of the USD against a basket of currencies.
- **S&P 500**: Represents the stock market index value.

Time span: **2014-01-02 to 2025-02-28** (11 years, 2804 observations).

The data collection process is documented in the Jupyter Notebook: `Gallagher_GoldPrice_Data_Collection_from_YFinance.ipynb`.

## Methodology
The project explores multiple time series forecasting methods, including:

- **ARIMA (AutoRegressive Integrated Moving Average)** 
- **LSTM (Long Short-Term Memory) Networks**
- **MLP (Multi-Layer Perceptron) Neural Network**
- **Prophet** 
- **ETS** 

The modeling process involves:

1. **Data Analysis:** Correlation analysis between gold price and macroeconomic variables, ACF & PACF analysis, stationarity, normality, volatility analysis for selecting appropriate transformation method and model selection.
2. **Data Preprocessing:** Handling missing values, outlier detection, data transformation (log-transformation, differencing), and normalization.
3. **Feature Engineering:** Incorporating macroeconomic indicators to enhance model performance.
4. **Model Training and Evaluation:** Splitting the data into training and testing sets, training the models, and evaluating their performance using metrics such as RMSE (Root Mean Square Error) and MAE (Mean Absolute Error).

Detailed analyses and results are available in the following notebooks:

- `Gallagher_Gold_Price_Only_Prediction.ipynb`: Models are trained using gold price only.
- `Gallagher_Gold_Price_with_Macroeconomic_Variables.ipynb`: Models are trained incorporating macroeconomic indicators--S&P 500, Oil Crude prices, and the US Dollar Index--to enhance model performance.

## Results
- LSTM networks with log-transformed gold prices and S&P 500 exhibited superior performance in capturing complex patterns and dependencies in the data (RMSE = 0.028).
- Incorporating macroeconomic factors significantly improved model accuracy.
- The project highlights the potential of deep learning in financial forecasting.

For more details, refer to the project documentation and presentation slides.

## Usage
1. Clone or extract the repository.
2. Install required dependencies using `pip install -r requirements.txt`.
3. Open Jupyter Notebook and navigate to the project directory.
4. Execute the notebooks in the following order:
   - `Gallagher_GoldPrice_Data_Collection_from_YFinance.ipynb`: Retrieves and merged the gold price and macroeconomics data from Yahoo Finance.
   - `Gallagher_Gold_Price_Only_Prediction.ipynb`: Data Preprocessing, Exploratory Data Analysis, and Model Development using Gold Price Only Data to Predict Gold Price
   - `Gallagher_Gold_Price_with_Macroeconomic_Variables.ipynb`: Analysis and Model Development using Gold Price and Macroeconomic Variables to Predict Gold Price

## Dependencies and Libraries
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
