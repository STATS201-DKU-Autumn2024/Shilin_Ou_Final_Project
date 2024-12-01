
# The Impact of Oil Price Fluctuations on Weighted Average Cost of Capital (WACC) within Energy Transition

## Authors
- **Shilin Ou**: Research design, data collection, and analysis.


## Disclaimer
This project was submitted as part of **STATS201: Machine Learning for Social Science**, instructed by **Prof. Luyao Zhang** at Duke Kunshan University in Autumn 2024.

## Acknowledgments
We extend our gratitude to:
- **Prof. Luyao Zhang** for guidance and insightful feedback.
- **Classmates** for collaborative discussions and support throughout the course.
- **AIGC tools** (e.g., ChatGPT, VADER, BERT) for enhancing sentiment analysis and report generation.
- The **open-source software community**, including libraries like TensorFlow, Scikit-learn, and Pandas, for providing essential tools for our analysis.

## Statement of Intellectual and Professional Growth
Through this project, I gained a comprehensive understanding of how machine learning and social science can intersect to address real-world challenges in the energy sector. I developed technical skills in sentiment analysis using VADER and BERT models, time-series forecasting with LSTM, and predictive modeling with Gradient Boosting. Moreover, this experience reinforced the importance of interdisciplinary approaches in solving complex problems and prepared me for future research and industry applications in sustainable energy and financial analytics.

## Embedded Media
### Demo Video
[[Watch the Demo Video](<link-to-demo-video>)](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/visualizations/demo_video_with_audio.mp4)

### Project Poster
https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/visualizations/Poster.png
## Table of Contents
1. [Abstract](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#abstract)
2. [ Background and Motivation:](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#background_and_motivation)
3. [Research Question](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#research_question)
4. [Application_Scenarios](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#application_scenarios)
5. [Methodology](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#methodology)
6. [Results](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#results)
7. [Intellectual Merit And Practical_impacts](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#intellectual_merit_and_practical_impacts)
8. [Practical_Impact](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#practical_impact)
9. [References](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#references)
10. [Appendix1](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Full_Report.md#appendix1)
11. [Statement of Intellectual and Professional Growth](#statement-of-intellectual-and-professional-growth)

## Navigation Instructions
This repository is organized as follows:

### [`Code`](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/tree/main/code)

- **Description**: Calculating WACC for different scenarios, performing sentiment analysis on news and visualizing keywords, predicting future WTI prices using an LSTM model, building a gradient boosting model to predict the average WACC based on WTI prices, and displaying the trend of WACC and WTI prices over time and the relationship between them.
- **[Overview](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/code/README.md#overview)**
- **[Files Included](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/code/README.md#files-included)**
- **[Prerequisites](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/code/README.md#prerequisites)**
- **[Usage Instructions](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/code/README.md#usage-instructions)**
- **[Expected Outputs](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/code/README.md#expected-outputs)**
  - [Detailed code](https://raw.githubusercontent.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/refs/heads/main/code/code_p1.ipynb)


### [`Data`](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/tree/main/data)
 - **Description**: The data used for this analysis comes from two primary sources: the global energy scenarios by Calcaterra et al. (2024) and WTI（West Texas Intermediate） spot price data from Iania et al. (2024).  
 - **[The source and purpose of the datase](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/data/README.md#the-source-and-purpose-of-the-datase)**
 - **[Preprocessing and harmonization step](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/data/README.md#preprocessing-and-harmonization-step)**
- **[Detailed Dataset](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/data/README.md#detailed-data)**
- **[Data Dictionary](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/data/README.md#data-dictionary)**

### [`Documentation`](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/tree/main/docs)
- **[Code Execution](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/README.md#code-execution)**
- **[Dependencies](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/README.md#dependencies)**
- **[Example Usage](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/README.md#example-usage)**

### [`Visualization`](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/tree/main/visualizations)

### [`System_Contiguration`](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/System_Configuration.md)


