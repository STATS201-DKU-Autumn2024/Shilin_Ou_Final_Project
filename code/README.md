# The impact of oil price fluctuations on Weighted Average Cost of Capital (wacc) within energy transition.

## Overview of the code
The code begins by loading historical WTI and energy scenario data. It processes this data by calculating the annual average WACC, derived from the maxwacc and minwacc for each scenario. An LSTM model is employed to forecast future WTI prices, which are then used to project future WACC values.

Then,The Gradient Boosting Regressor is used to model the relationship between WTI prices and WACC, with the model's performance evaluated using R-squared and Mean Squared Error metrics.The results are visualized to highlight the trends and relationships, aiding in long-term energy transition planning.

## Purpose
The code's primary goal is to analyze and model the relationship between oil prices (WTI) and the Weighted Average Cost of Capital (WACC) under various energy transition scenarios. It achieves this by calculating annual average WACC values based on maxwacc and minwacc, then applying machine learning models (Gradient Boosting Regressor and LSTM) to predict future values and understand correlations.

## Result
The analysis reveals a clear trend of decreasing WACC values from 2020 to 2100, with the WACC reducing from 7.68% in 2020 to 5.58% in 2100, reflecting the long-term reduction in the cost of capital across the energy transition scenarios. Using a Gradient Boosting Regressor, the relationship between WTI prices and WACC was modeled. The model yielded an R-squared value of 0.1977, indicating a correlation between WTI price fluctuations and WACC changes. The Mean Squared Error (MSE) was 0.0002, suggesting reasonable accuracy in predictions, although further model refinement may be necessary. The feature importance of WTI prices was recorded as [1.], implying that, in this model, WTI prices were the sole factor influencing WACC.


<img width="1019" alt="image" src="https://github.com/user-attachments/assets/ee1d2306-d22b-4bc4-af77-5d47e750d4bc">

Table1: Predicted WTI price and WACC value over time(2020-2100)

<img width="970" alt="image" src="https://github.com/user-attachments/assets/be0ff7d2-9758-4a4f-96ad-0cce44d20306">

Table2: The relationship between WTI price and WACC value

