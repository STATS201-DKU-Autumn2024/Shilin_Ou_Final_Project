# Title: The impact of oil price fluctuations on Weighted Average Cost of Capital (wacc) within energy transition.

## Background_and_Motivation

Volatility in oil prices brings uncertainty to energy transition projects and affects the capital cost for investors. Fluctuations in oil prices also influence the relative competitiveness of various energy sources such as natural gas, coal, and renewables, thus affecting investment patterns and the capital costs related to energy projects (Lin & Cheung, 2024). A comprehensive understanding of the implications of oil price volatility is necessary as it enhances risk management strategies and shapes investment decisions in the energy transition field.

Previous studies have proved that various aspects can play a role in shaping the weighted average cost of capital (WACC) of energy transition. For instance, mature technologies benefit from lower costs due to reduced risks, while emerging ones face higher costs due to market uncertainties (Egli et al., 2021). Policy and regulatory risks also impact WACC. Clear subsidies and stable frameworks lower costs for renewable technologies, while stricter emission regulations raise costs for fossil fuels (Zhou et al., 2021). Moreover, country-specific risks, like economic stability and investment environments, cause disparities, with developed nations having lower WACC than emerging economies. Different energy technologies have different WACC levels. Renewables require higher initial investments and are thus more sensitive to capital costs (Polzin et al., 2021).
  
Similarly, the impact of oil price fluctuations on WACC is a complex issue that has been studied in various academic works. Studies (Calcaterra et al., 2024) emphasize the importance of fair finance in ensuring energy availability and sustainability. Empirical analyses have shown that the cost of capital (CoC) varies across countries and technologies, and developing countries often have higher CoC due to higher perceived risks (Fuso Nerini et al., 2017). Integrating these financial dynamics into climate policy and the energy transition is crucial for understanding the implications of oil price volatility on investment decisions and the global shift towards sustainable energy sources.

## Research_Question

This study aims to explore the intersection of social science and machine learning by analyzing how oil price trends affect market perceptions, risk assessments, and financing decisions for renewable energy. Specifically, it focuses on how fluctuations in oil prices influence the Weighted Average Cost of Capital (WACC) for energy transition projects in the future. By using social science frameworks to examine societal and policy responses, along with machine learning models for forecasting oil prices and simulating investment scenarios, the research intends to provide a comprehensive understanding of how oil price volatility shapes the financial landscape of energy transition and the associated cost of capital.

## Application_Scenarios

The dataset for this study comes from industries closely linked to the energy sector, such as renewable energy, fossil fuels, and finance. Data sources include historical oil price datasets from global energy markets (e.g., Brent Crude and WTI prices), investment cost data for renewable technologies (e.g., solar, wind, and hydropower), and financial metrics like the Weighted Average Cost of Capital (WACC) across different energy projects. These datasets are directly in line with the research question as they help analyze the relationships between oil price volatility, market perceptions, and WACC in energy transition projects. Historical oil price trends are essential for forecasting future volatility using machine learning models, while financial data on investment costs and WACC allow for scenario simulations of how different oil price levels affect capital allocation

Consequently, Energy companies can use these findings to make strategic investment decisions, and policymakers can formulate regulations to stabilize the impact of oil price volatility on energy financing. Financial institutions will benefit from a clearer understanding of the associated risks, allowing for more informed investment strategies. Moreover, this research supports sustainable development goals by ensuring accessible energy financing, especially in developing countries, and helps mitigate climate change by influencing the pace of the global shift towards low-carbon energy systems.

## Methodology

As illustrated in Figure 1, the methodology encompasses three key stages. First, the study calculates the average WACC values based on the research data of Calcaterra et al. (2024). We collect the maximum weighted average cost of capital (maxWACC) and the minimum weighted average cost of capital (minWACC) for each scenario in Calcaterra et al.’s (2024) study. Assuming that the weight of each scenario is equal, we calculate the average of the annual WACC of all scenarios.

Next, sentiment analysis was conducted. We used natural language processing (NLP) methods, combined with VADER and BERT models to analyze social media texts and news articles related to WTI oil prices. The VADER model is suitable for processing short texts and can calculate sentiment scores for each article, ranging from -1 (extremely negative sentiment) to +1 (extremely positive sentiment), which is particularly suitable for social media comments and news headlines. The BERT model, through fine-tuning, has shown strong capabilities in sentiment analysis tasks, especially its bidirectional encoding ability, which enables it to deeply capture subtle emotional changes in text and improve the accuracy of sentiment classification. To enhance the interpretability of the model, attention visualization techniques were also employed, helping understand how specific words influenced sentiment scores.
  
Then, historical WTI oil prices are used to forecast future prices with the long short-term memory (LSTM) model, which is a type of recurrent neural network (RNN), to predict WTI oil prices. Unlike traditional RNNs, this model overcome the vanishing gradient problem with gates (input, forget, and output) controlling information flow. This enables LSTMs to model complex, non-linear relationships in time-series data, making it suitable for financial data with short-term fluctuations and long-term trends. Specifically, it can learn long-term dependencies and patterns in the data, essential for capturing the cyclical and volatile nature of oil prices. In this code, two LSTM layers extract hierarchical temporal features from historical WTI price data (Iania et al., 2024), capturing long-term dependencies and trends. The sentiment analysis results were also incorporated as additional input features to improve the forecast's accuracy and reliability.
  
Finally, as shown in Figure 1, the Gradient Boosting Regressor was employed to predict the average WACC based on the forecasted WTI oil prices. Model evaluation metrics such as R-squared and MSE were used to assess the performance. Visualization techniques, including dual-axis charts and scatter plots, demonstrated trends and relationships between WTI prices and WACC.
  
The combination of machine learning models, sentiment analysis, and visualization constituted a robust framework for analyzing the relationship between WTI prices and WACC, laying the foundation for an in-depth exploration of their impact.

## Results

Based on the methodology, the analysis shows that WTI-represented oil prices have a moderate effect on the WACC in the energy transition sector. The Gradient Boosting model, trained to predict WACC only based on WTI prices, got an R-squared value of 0.1977, meaning that about 20% of the WACC variation can be attributed to oil price fluctuations. Though the MSE is low, this indicates the model's limited ability to predict WACC just from WTI, stressing that while there is some correlation, it's not the main factor.

This moderate R-squared value indicates that WTI prices likely contribute to variations in WACC, potentially influencing capital costs by affecting investor sentiment and energy market dynamics. However, WTI prices are not the dominant drivers. Other factors—such as market uncertainties (Egli et al., 2021), policy and regulatory risks (Zhou et al., 2021), and advancements in technologies (Polzin et al., 2021)—appear to play a more substantial role in shaping financing costs for energy transition projects.

## Intellectual_Merit_and_Practical_Impacts

This research improves the existing literature by integrating machine learning and social science to study how oil price fluctuations affect the Weighted Average Cost of Capital (WACC) in energy transition projects. Based on previous studies like Calcaterra et al. (2024), which show the differences in financing costs among countries, and Zhou et al. (2021), which stress the role of policy in shaping WACC, this study adds value by including machine learning techniques such as sentiment analysis (VADER and BERT) and predictive modeling (LSTM and Gradient Boosting). By combining these methods with social science insights, the research offers a unique, interdisciplinary way to understand the financial and behavioral impacts of oil price volatility, helping to have a deeper understanding of WACC dynamics in renewable energy.

The study also finds areas for future exploration, dealing with key limitations that inspire new research. For example, although the results suggest a moderate correlation between oil prices and WACC, further work could explore the role of other influential factors, such as technological advancements (Polzin et al., 2021) or economic stability (Fuso Nerini et al., 2017). Expanding the dataset to include real-time data streams or looking into regional differences in WACC drivers would provide more detailed insights. Moreover, the ethical challenges pointed out, such as biases in data and accountability in AI-driven decision-making, are in line with the calls for fair and transparent financing tools (Egli et al., 2021). Future research could explore causal inference techniques or policy simulations to discover how targeted interventions, like subsidies or carbon pricing, influence WACC, contributing to the wider field of sustainable energy transition financing.

## Practical_Impact

This study furnishes actionable insights into the way oil price fluctuations influence the Weighted Average Cost of Capital (WACC) in energy transition projects, proffering substantial benefits for both industry and policy. Energy companies can leverage these findings to formulate resilient investment strategies and allocate resources efficaciously between fossil fuels and renewables. Policymakers can devise adaptive regulations, such as dynamic subsidies or carbon pricing, to stabilize renewable energy financing, facilitating a smoother transition to sustainable energy systems.

Industries can incorporate the study’s machine learning models into risk management frameworks, enhancing oil price forecasting and investment decision-making. Governments and financial institutions can refine energy policies and financing tools, such as green bonds, to diminish WACC disparities, particularly in developing economies. These applications ensure a more stable and efficient energy transition, advancing global climate and sustainability goals.

However, the large-scale deployment of AI-driven solutions gives rise to governance and ethical challenges. Bias in training data, such as the overrepresentation of trends from developed markets, may lead to inaccurate recommendations for developing countries, where investment risks and financing dynamics are different. Sentiment analysis, which relies on public data from news and social media, must also follow privacy regulations like GDPR to protect individual rights. Moreover, errors in AI-driven forecasts of oil prices or WACC could mislead policymakers and investors, causing inefficient resource allocation or ineffective regulations. Regular audits of models, transparency in their methodologies, and integration with expert input are necessary to ensure reliability and trust. Inclusive governance frameworks should also deal with systemic inequalities in access to financing, making sure AI technologies promote fair and responsible energy transitions globally.

## References
Calcaterra, M., Reis, L. A., P. Fragkos, T. Briera, de, S., Egli, F., Emmerling, J., Iyer, G., Mittal, S., Polzin, J., Sanders, L., Schmidt, T. S., A. Serebriakova, Steffen, B., van, Vuuren, van, Waidelich, P., & M. Tavoni. (2024). Reducing the cost of capital to finance the energy transition in developing countries. Nature Energy. https://doi.org/10.1038/s41560-024-01606-7

Egli, F., Steffen, B., Polzin, F., & Schmidt, T. S. (2021). The effect of differentiating costs of capital by country and technology on the European energy transition. Climatic Change, 167(26). https://doi.org/10.1007/s10584-021-03163-4

Fuso Nerini, F., Tomei, J., To, L. S., Bisaga, I., Parikh, P., Black, M., Borrion, A., Spataru, C., Castán Broto, V., Anandarajah, G., Milligan, B., & Mulugetta, Y. (2017). Mapping synergies and trade-offs between energy and the Sustainable Development Goals. Nature Energy, 3(1), 10–15. https://doi.org/10.1038/s41560-017-0036-5

Iania, L., Lyrio, M., & Nersisyan, L. (2024). Oil price shocks and bond risk premia: Evidence from a panel of 15 countries. Energy Economics, 107940–107940. https://doi.org/10.1016/j.eneco.2024.107940

Polzin, F., Sanders, M., Steffen, B., Egli, F., Schmidt, T. S., Karkatsoulis, P., ... & Paroussos, L. (2021). The effect of differentiating costs of capital by country and technology on the European energy transition. Climatic Change, 167, 1-21.

Lin, Y., & Cheung, A. (Wai K. (2024). Climate policy uncertainty and energy transition: Evidence from prefecture-level cities in china. Energy Economics, 139, 107938. https://doi.org/10.1016/j.eneco.2024.107938

Zhou, X., Wilson, C., & Caldecott, B. (2021). The energy transition and changing financing costs. Oxford Review of Economic Policy.

## Appendix1
### Discussion about other machine learning methods
#### Explanation:
Natural Language Processing (NLP) methods, such as VADER and BERT, can assist in analyzing public sentiment and social perceptions concerning oil price changes. By extracting sentiment scores from social media, news articles, and policy reports, these methods can elucidate the psychological and societal drivers underlying investment behaviors and market dynamics. NLP techniques enable the study to contextualize quantitative results by revealing how investor sentiment or public discourse contributes to shifts in the Weighted Average Cost of Capital (WACC), providing enhanced interpretability for financial data.

#### Causal Inference
Causal inference can improve the study by isolating the direct effect of oil price fluctuations on the Weighted Average Cost of Capital (WACC) for energy transition projects. Methods like propensity score matching or instrumental variables can be used to estimate the causal impact of exogenous oil price changes, like those driven by geopolitical shocks, on financing costs. Additionally, difference-in-differences (DiD) analysis can evaluate how oil price shocks influence WACC trends by comparing changes before and after such events in different energy sectors. Machine learning-based causal methods, such as causal forests, can reveal heterogeneous effects, showing how these impacts vary across technologies, countries, or market conditions. These approaches allow the study to go beyond correlation, providing solid insights into the causal relationships driving investment decisions in the energy transition.

#### Optimization:
Reinforcement learning (RL)can optimize the hyperparameters of the LSTM model used to predict oil prices, like learning rates or the number of layers, through a reward function based on the model's prediction error. This ensures the LSTM adapts to complex time-series data more effectively. Similarly, RL can simulate the best investment strategies for energy companies, adjusting capital allocation between renewable and fossil fuel projects based on forecasted oil prices and WACC. For instance, the agent could learn to prioritize renewable energy investments when oil price volatility increases the perceived risk of fossil fuel projects. RL can also improve the integration of sentiment analysis data into the Gradient Boosting model by dynamically weighting sentiment features, such as positive or negative public reactions, to enhance WACC prediction accuracy. These practical applications make RL a powerful tool for refining models and strategies in the energy transition.

