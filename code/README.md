# The impact of oil price fluctuations on Weighted Average Cost of Capital (wacc) within energy transition.

## Overview 

The purpose of this code is to study the impact of future WTI prices on the weighted average cost of capital (WACC) in the process of energy transition. By predicting WTI prices in different scenarios and combining WACC calculation and analysis, the code provides a comprehensive approach to explore the relationship between market sentiment, historical data, and future capital costs in the energy economy. Specific tasks include: calculating WACC for different scenarios, performing sentiment analysis on news and visualizing keywords, predicting future WTI prices using an LSTM model, building a gradient boosting model to predict the average WACC based on WTI prices, and displaying the trend of WACC and WTI prices over time and the relationship between them.

## Files Included

1. Future_wti_predictions.csv.  
Functionality: Contains the predicted future WTI prices from a trained LSTM model. This file stores the historical and predicted price data along with associated years.

2. Global_Energy_Scenario——Data.csv  
Functionality: This dataset contains information about global energy scenarios, including the maximum and minimum WACC values for each year. The code calculates the average WACC (avgwacc) from these values for use in modeling.

3. Annual_wacc.csv  
Functionality: This file contains annual WACC data, which is used to analyze how changes in WACC affect WTI prices over time. It includes columns such as the year and average WACC.

4. Sentiment_analysis.py  
Functionality: This script fetches news articles related to WTI oil using NewsAPI, performs sentiment analysis using the VADER sentiment analysis tool from NLTK, and calculates an average sentiment score for the news articles.

5. Prediction_model.py  
Functionality: This file contains code for training and evaluating a Gradient Boosting Regressor model to predict WACC based on the predicted WTI prices. The model is trained, and performance metrics like R-squared and MSE are calculated.

6. Visualizations.py  
Functionality: This script generates visualizations for the analysis, including:
Dual y-axis plot comparing WTI prices and WACC over time.
Scatter plot with a linear regression fit for WTI price vs. WACC based on different datasets (annual WACC and global scenario WACC).

## Prerequisites
Python Version:  
Python 3.9 or higher is recommended for compatibility with all libraries.

Required Libraries:  
pandas: 1.3.0 or higher  
numpy: 1.21.0 or higher  
matplotlib: 3.4.0 or higher  
seaborn: 0.11.0 or higher  
scikit-learn: 0.24.0 or higher  
tensorflow: 2.5.0 or higher  
nltk: 3.6.0 or higher  
requests: 2.25.0 or higher  


Table1: Predicted WTI price and WACC value over time(2020-2100)


Table2: The relationship between WTI price and WACC value



