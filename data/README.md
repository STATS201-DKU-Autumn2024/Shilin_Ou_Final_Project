#  The impact of oil price fluctuations on Weighted Average Cost of Capital (wacc) within energy transition.

## The source and purpose of the datase
The data used for this analysis comes from two primary sources: the global energy scenarios by Calcaterra et al. (2024) and WTI（West Texas Intermediate） spot price data from Iania et al. (2024). 

The purpose of using the dataset is to predict the trend of WTI (West Texas Intermediate) spot oil prices from 2025 to 2100 by collecting historical WTI spot oil price data. Specifically, the historical WTI spot oil price data in Iania et al. (2024) will be used for machine learning modeling to predict the future trend of WTI oil prices. Then, these predicted results will be integrated with the WACC (weighted average cost of capital) forecast results in Calcaterra et al. (2024), which represent the economic conditions under different energy transition scenarios.

The main goal of this analysis is to explore the impact of WTI oil price fluctuations on future WACC, especially in the context of energy transition. By comparing the predicted WTI oil prices with the estimated WACC results, we can analyze the potential impact of oil price fluctuations on capital costs, which is a key factor in energy infrastructure investment decision-making. This analysis will provide important insights to help us understand how oil price fluctuations affect the formulation of future energy transition strategies and changes in the financing environment.
## Preprocessing and harmonization step

The Calcaterra et al. (2024) dataset encompasses WACC (weighted average cost of capital) values for diverse energy scenarios, which are represented by the annual "maxwacc" and "minwacc" values for each scenario. These values are averaged to obtain an annual estimate of WACC, guaranteeing that the weight of each scenario is identical, thereby reducing bias in the analysis.

The Iania et al. (2024) dataset comprises historical spot WTI prices, with data columns including "Date" and "Real WTI Spot Price". The preprocessing steps involve converting the "Date" column to a date-time format and setting it as the index of the dataset. Subsequently, the real WTI spot price is normalized using the minimum-maximum normalization method, converting the numerical values to a uniform range from 0 to 1 for robust and unbiased model training.
 

## Detailed Data
The DataSet of wacc: https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet1/blob/main/data/Global_Energy_Scenario——Data.csv

The DataSet of WTI price: https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet1/blob/main/data/WTI_price.xlsx

The Dataset of average anual Wacc values after process Calcaterra et al.'s (2024) dataset:https://raw.githubusercontent.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/refs/heads/main/data/annual_wacc.csv

The Dataset of future WTI price prediction after processing Iania et al.'s (2024) dataset: https://raw.githubusercontent.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/refs/heads/main/data/future_wti_predictions.csv

## Data Dictionary 

| Variable Name              | Data Type | Description                                                                                      | Source File                                 | Unit       | Range                        | Remarks                                                         |
|---------------------------|-----------|------------------------------------------------------------------------------------------------------|---------------------------------------------|------------|------------------------------|-----------------------------------------------------------------|
| Region                    | String    | The name of the region, referring to different countries or areas                                   | Global_Energy_Scenario——Data.csv             | -          | -                            | -                                                                |
| minwacc                   | Float     | The minimum Weighted Average Cost of Capital (WACC)                                               | Global_Energy_Scenario——Data.csv             | -          | 0.0 - 0.1                   | Represents the capital costs of energy transition projects in different regions |
| maxwacc                   | Float     | The maximal Weighted Average Cost of Capital (WACC)                                               | Global_Energy_Scenario——Data.csv             | -          | 0.0 - 0.1                   | Represents the capital costs of energy transition projects in different regions |
| Real RAC                 | Float     | The actual rate of return, used to calculate the relationship between bond risk premiums and actual returns | Oil price shocks and bond risk premia: Evidence from a panel of 15 countries | -          | -                            | -                                                                |
| Global Oil Production      | Float     | Global crude oil production, measured in million barrels per day                                 | Oil price shocks and bond risk premia: Evidence from a panel of 15 countries | million barrels/day | 70 - 100                 | Reflects the supply situation in the global crude oil market                      |
| Real WTI Spot Price       | Float     | The real West Texas Intermediate (WTI) spot price, adjusted for inflation                           | Oil price shocks and bond risk premia: Evidence from a panel of 15 countries | -          | 20 - 70                    | Reflects changes in global crude oil market prices                              |
| OECD+6NME IP            | Float     | The industrial production index for OECD countries and six major non-member economies               | Oil price shocks and bond risk premia: Evidence from a panel of 15 countries | -          | 50 - 150                   | Reflects the level of global economic activity and its impact on bond risk premiums    |
| Delta Inventories         | Float     | The change in oil inventories as a fraction of the previous period's oil production                   | Oil price shocks and bond risk premia: Evidence from a panel of 15 countries | %          | -10% - 10%                 | Reflects changes in global oil inventory levels and their impact on bond risk premiums |
| Cost of Capital (CoC)     | Float     | The cost of capital, reflecting the return on investment required for project risks                  | Reducing the cost of capital to finance the energy transition in developing countries                              | Percentage  | 5% - 15%                   | On average, 4% higher in high-CoC regions compared to low-CoC regions               |
| Technology                | String    | Type of technology, such as renewable energy technology                                        | Reducing the cost of capital to finance the energy transition in developing countries                               | -          | -                            | -                                                                |
| Financing Cost            | Float     | The cost of financing, referring to the cost paid by a project to obtain funds                      | Reducing the cost of capital to finance the energy transition in developing countries                             | -          | 0.01 - 0.1                  | Includes debt and equity costs, affecting investment decisions in energy transition projects |
| Country Risk              | Float     | Country risk, reflecting additional risks when investing in a specific country                   | Reducing the cost of capital to finance the energy transition in developing countries                               | Percentage  | 0.05 - 0.2                  | A component affecting the cost of capital                                    |
| Technology Risk           | Float     | Technology risk, reflecting risks associated with specific technologies                            | Reducing the cost of capital to finance the energy transition in developing countries                               | Percentage  | 0.01 - 0.05                 | A component affecting the cost of capital, decreasing with technology maturity       |
| Debt Share                | Float     | The proportion of debt that a project or company can attract                                    | Reducing the cost of capital to finance the energy transition in developing countries                              | -          | 0 - 1                       | Used to calculate the Weighted Average Cost of Capital                         |
| Equity Cost               | Float     | The cost of equity, the internal rate of return expected by the asset owner                      | Reducing the cost of capital to finance the energy transition in developing countries                               | -          | 0.05 - 0.2                  | Used to calculate the Weighted Average Cost of Capital                         |
| Interest Expense          | Float     | Interest expenses, used to calculate debt costs                                                | Reducing the cost of capital to finance the energy transition in developing countries                             | -          | 0.01 - 0.1                  | Reflects the interest paid by a company on loans                             |
| Dividends Paid            | Float     | Cash dividends paid, used to calculate equity costs                                            |Reducing the cost of capital to finance the energy transition in developing countries                            | -          | 0 - 1                       | Reflects the profits distributed by a company to its shareholders               |

## Refferences

Calcaterra, M., Reis, L. A., P. Fragkos, T. Briera, de, S., Egli, F., Emmerling, J., Iyer, G., Mittal, S., Polzin, J., Sanders, L., Schmidt, T. S., A. Serebriakova, Steffen, B., van, Vuuren, van, Waidelich, P., & M. Tavoni. (2024). Reducing the cost of capital to finance the energy transition in developing countries. Nature Energy. https://doi.org/10.1038/s41560-024-01606-7

Iania, L., Lyrio, M., & Nersisyan, L. (2024). Oil price shocks and bond risk premia: Evidence from a panel of 15 countries. Energy Economics, 107940–107940. https://doi.org/10.1016/j.eneco.2024.107940


