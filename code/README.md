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

## Usage Instructions

1. Calculate the Average WACC  
This step calculates the annual WACC for each scenario by averaging the maxwacc and minwacc values from Calcaterra et al. (2024). Then, it computes the average WACC across all scenarios for each year, providing the base data for subsequent analysis.

2. Sentiment Analysis and Visualization (NLP)  
This step uses the VADER (Valence Aware Dictionary and sEntiment Reasoner) algorithm for sentiment analysis of short texts, like news articles. It calculates sentiment scores ranging from -1 (negative) to +1 (positive) based on the words and punctuation. Additionally, a word cloud is generated to visualize the most frequent terms in the articles, helping identify key themes. Combining sentiment analysis with word cloud visualization, the code provides both quantitative sentiment scores and qualitative insights into the main topics, offering a comprehensive analysis of public sentiment and key discussions surrounding WTI oil prices.

3. Predicting Future WTI Prices (LSTM)
This step uses an LSTM model to predict future WTI spot prices based on historical data from Iania et al. (2024). The data is preprocessed, normalized, and converted into sequences for training. After training, the model predicts WTI prices at five-year intervals from 2020 to 2100. Additionally, sentiment analysis is applied to news articles about WTI oil, and the resulting sentiment scores are used to gauge market sentiment, which may influence the price predictions.

4. Predicting Average WACC Based on WTI Prices
This step builds and evaluates a Gradient Boosting Regressor model to predict the average Weighted Average Cost of Capital (WACC) based on predicted WTI prices. The code loads the WTI price predictions and global energy scenario data, calculates the average WACC for each year, and merges the data. After splitting the data into training and testing sets, the model is trained to predict the average WACC. The model’s performance is evaluated on the test set, providing valuable insights for future financial decisions and analysis.

5. Trends of WACC and WTI Prices Over Time  
This step generates a dual-axis plot to visualize the relationship between WTI prices and annual WACC over time. The left y-axis represents the annual WACC, ranging from 0 to 0.1, shown with a red line, while the right y-axis represents WTI prices, limited to the range of 24 to 30, shown with a blue line.

6. Relationship Between Predicted WTI Prices and WACC
This step visualizes the relationship between predicted WTI prices and WACC using two data sources: annual WACC data and global energy scenario data. After loading and processing these datasets, they are merged based on the year. The plot displays scatter points for WTI vs. annual WACC (in red) and WTI vs. scenario WACC (in blue). A linear regression line with a confidence interval is added for the annual WACC data. Each data point is annotated with its corresponding year, enhancing the readability of the time trends and helping to better analyze the evolution of the data.

## Expected Outputs

The analysis shows that oil prices, represented by WTI, have a moderate influence on the Weighted Average Cost of Capital (WACC) in the energy transition sector, though not being the main factor. The Gradient Boosting model, trained to predict WACC based only on WTI prices, got an R-squared value of 0.1977, indicating that about 20% of the variation in WACC can be explained by oil price fluctuations. While the Mean Squared Error (MSE) is low, this reflects the model's limited ability to predict WACC solely from WTI, highlighting that although there is some correlation, it is not strong.

The dual-axis line plot and scatter plot with a linear regression fit show some correlation patterns between WTI and WACC over time, but they are not extremely strong, reinforcing the statistical findings. Overall, while oil prices do have an impact on WACC to some extent, a broader set of economic, policy, and technological variables must also be considered when evaluating capital costs for energy transition financing.

<img width="422" alt="image" src="https://github.com/user-attachments/assets/e2c8ded1-4a0d-4723-b021-8b9ed3fb2ae3">


Table1: Sentiment Distribution for WTi Oil News Articles

<img width="1009" alt="image" src="https://github.com/user-attachments/assets/64b403d1-3706-4bc6-aaa1-b5a0aa9157c1">


Table2: Predicted WTI price and WACC value over time(2020-2100)

<img width="967" alt="image" src="https://github.com/user-attachments/assets/2b080476-dcbe-4ef1-9284-fdd262ca10b3">

Table3: The relationship between WTI price and WACC value

## Contributors
1. Calcaterra et al. (2024): provide the dataset and evaluation modle of wacc.

2. Iania et al. (2024): provide thw historical dataset of wti.

3. Shilin Ou: write the code to process the data.

Detailed code: https://raw.githubusercontent.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/refs/heads/main/code/code_p1.ipynb
