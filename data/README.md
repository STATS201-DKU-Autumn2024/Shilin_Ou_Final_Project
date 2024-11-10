#  The impact of oil price fluctuations on Weighted Average Cost of Capital (wacc) within energy transition.

## Summary for the data
  The data used for this analysis comes from two primary sources: the global energy scenarios by Calcaterra et al. (2024) and WTI（West Texas Intermediate） spot price data from Iania et al. (2024). For the WACC (Weighted Average Cost of Capital) analysis, annual WACC values were calculated by averaging the 'maxwacc' and 'minwacc' values for each scenario in Calcaterra et al.'s research, representing varying economic conditions. To avoid bias, equal weighting was assumed across all scenarios, resulting in an average WACC per year.
  
For the WTI spot price data, historical values were extracted from an Excel file(Iania et al., 2024) and focused on columns containing Date and Real WTI Spot Price. The Date column was converted to datetime format and set as the DataFrame index. To ensure consistency for machine learning models, the WTI spot prices were normalized using min-max scaling, transforming the data to a range between 0 and 1. This preprocessing supports robust, unbiased model training.

## Detailed Data
The DataSet of wacc: https://raw.githubusercontent.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet1/refs/heads/main/data/Global_Energy_Scenario——Data.csv

The DataSet of WTI price:
