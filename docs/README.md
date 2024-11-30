
## Code Execution

#### Install Required Python Dependencies:
Ensure Python is installed on your system.
Install the required libraries using pip. The list of libraries is provided below under "Dependencies."
#### Download NLTK Data:
Open Python and run the command to download the necessary data for sentiment analysis. This includes the vader_lexicon.
Install FFmpeg:
FFmpeg is required to create and edit videos.
On macOS, install FFmpeg via Homebrew.
On Ubuntu, install it using the package manager.
On Windows, download FFmpeg from its official website, install it, and ensure it is added to your system's PATH.
#### Prepare Input Files:
Place the following input files in the same directory as your script:  
A file containing WTI price data (e.g., an Excel file with date and real WTI spot prices).  
A global energy scenario data file (e.g., a CSV file containing year, scenario, and WACC values).  
Optionally, provide a background music file in .ogg format for use in video creation.
#### Update File Paths in the Script:
Edit the script to ensure the file paths point to the correct location of your input files.  
#### Run the Script:
Save the script as a Python file and execute it through your terminal or command prompt.  
#### Review the Outputs:  
A CSV file containing predicted WTI prices.  
Visualization videos (with and without background music).  

## Dependencies

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

## Poster and Report
The proposal report：https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Shilin_Ou_Final_Proposal.docx


Poster：https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/poster
