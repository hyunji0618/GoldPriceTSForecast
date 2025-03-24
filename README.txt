Gallagher Gold Price Prediction
================================

## Project Description
This project aims to predict global gold prices using time series forecasting techniques. Various models, including LSTM, MLP(NN), ARIMA, ETS, and Prophet, were explored to identify the best-performing model. The model leverages macroeconomic indicators such as S&P 500, Oil Crude prices, and the US Dollar Index to enhance prediction accuracy.

## Authors
- **Amy Kim**
- **Cicily Mathew**
- **Olivia Rumere**

## Institution
- **Course:** Time Series Analysis and Forecasting
- **Instructor:** Fan Yang
- **University:** University of Chicago
- **Date:** March 11, 2025

## How to Run the Notebooks
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

## Dataset Explanation
The dataset consists of historical gold prices along with macroeconomic indicators:
- **Gold Price**: The target variable, measured in USD per ounce.
- **Oil Crude**: Crude oil prices in USD per barrel.
- **US Dollar Index**: Measures the strength of the USD against a basket of currencies.
- **S&P 500**: Represents the stock market index value.

Time span: **2014-01-02 to 2025-02-28** (11 years, 2804 observations).

## Model Insights
- LSTM with log-transformed gold prices and S&P 500 achieved the best performance (RMSE = 0.028).
- Incorporating macroeconomic factors significantly improved model accuracy.
- The project highlights the potential of deep learning in financial forecasting.

For more details, refer to the project documentation and presentation slides.
