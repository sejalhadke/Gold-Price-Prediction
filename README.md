## Gold Price Prediction for the Next 30 Days

## Project Overview

This project focuses on forecasting gold prices for the next 30 days using time series analysis and machine learning techniques. The goal was to build a model that accurately predicts future gold prices based on historical data. 

The project involved the following key stages:

* **Data Collection and Preprocessing:** Gathering historical gold price data and preparing it for analysis.
* **Exploratory Data Analysis (EDA):** Analyzing the data to understand its characteristics, including trends, seasonality, and potential outliers.
* **Model Building:** Developing and comparing different time series forecasting models.
* **Model Evaluation:** Assessing the performance of the models using appropriate metrics.
* **Deployment:** Creating a web application for easy forecasting of gold prices.

## Project Objectives

* To understand the underlying structure in the gold price dataset.
* To develop a suitable forecasting model for predicting gold prices for the next 30 days. 

## Data Description

The dataset consists of 2182 observations and 2 features. The key features include:

* **Date:** The date for the gold price observation (originally an object type, converted to datetime format). 
* **Price:** The price of gold.
  
## Exploratory Data Analysis (EDA)

The EDA process involved the following:

1.  **Data Conversion:** Converting the 'Date' column to the correct datetime format. 
2.  **Indexing:** Setting the 'Date' column as the index to facilitate time series analysis. 
3.  **Data Cleaning:**
    * Checking for and handling null values (none found). 
    * Checking for and handling duplicate values (none found). 
    * Identifying and removing outliers using boxplots and filtering. 
4.  **Visualization:** Visualizing the data to identify trends and seasonality.  Seasonality was observed.

## Time Series Decomposition

Time series decomposition was performed to analyze the following components:

* **Trend:** Long-term movements in the data. 
* **Seasonality:** Recurring patterns within a fixed time period. 
* **Residuals:** The random or irregular component of the time series data. 

## Model Building

Several models were explored for gold price forecasting:

* ARIMA
* LSTM
* FBProphet

The FBProphet model was ultimately chosen as the deployment model due to its superior performance. 

## Model Evaluation

The models were evaluated using the following metrics:

* **R-squared (R2) Score:** A measure of how well the model fits the data.
* **Mean Absolute Error (MAE):** The average absolute difference between predicted and actual values.
* **Root Mean Squared Error (RMSE):** A measure of the overall prediction error.

Here's a comparison of the model performances:

| Model Name | R2 Score | MAE Value | RMSE Value |
| ---------- | -------- | --------- | ---------- |
| ARIMA      | 0.97     | 57.22     | 14022.37   |
| LSTM       | -119.13  | 1549.82   | 2500049.65 |
| FBProphet  | 0.95     | 111.61    | 28354.73   | 

## Deployment

The FBProphet model was deployed using Streamlit, a Python framework for building interactive web applications. 

* Streamlit was used to create a user-friendly web interface. 
* The web app allows users to select a date range for generating gold price forecasts. 

## Web Application Features

* Interactive date range selection for forecasting.
* Display of the forecasted gold price table.
 
## Project Architecture/Flow

1.  **Data Acquisition:** Obtain historical gold price data.
2.  **Data Preprocessing:** Clean, transform, and prepare the data for analysis.
3.  **Exploratory Data Analysis (EDA):** Analyze data characteristics and visualize patterns.
4.  **Model Selection:** Choose appropriate time series forecasting models.
5.  **Model Training:** Train the selected model on the historical data.
6.  **Model Evaluation:** Evaluate model performance using relevant metrics.
7.  **Deployment:** Deploy the best-performing model as a web application using Streamlit.
8.  **Forecasting:** Use the deployed model to predict gold prices for the next 30 days. 

## Installation

To run this project, you will need to have Python and the following libraries installed:

* pandas
* matplotlib
* scikit-learn
* Prophet
* Streamlit

You can install the required packages using pip:
```bash
pip install pandas matplotlib scikit-learn Prophet streamlit
```


## Usage
* Clone the repository.
* Install the required libraries.
* Run the Streamlit application:

```bash
streamlit run your_streamlit_app.py
```
* Use the web interface to select the date range and generate gold price forecasts.






