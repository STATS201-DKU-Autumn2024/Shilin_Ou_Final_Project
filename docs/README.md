
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

Detaied code explanation and instruction: [[https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/tree/main/docs](https://raw.githubusercontent.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/refs/heads/main/code/README.md)](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/code/README.md)
## Dependencies

Make sure the following libraries are installed:

pandas for data manipulation  
numpy for numerical operations  
matplotlib and seaborn for visualizations  
tensorflow for building and training the LSTM model  
nltk for sentiment analysis  
requests for fetching news data  
wordcloud for generating word clouds  
scikit-learn for regression and performance evaluation  


## Example Usage

### Full Workflow
Prepare the required data files, including WTI prices and global energy scenarios.  
Update file paths in the script to match your input data locations.  
Run the script to generate predictions, analyze sentiment, create visualizations, and produce video outputs.  
### Individual Components  
Use the WTI price data to train a prediction model.  
Fetch and analyze news sentiment based on provided queries and dates.  
Visualize WTI prices and WACC values using line plots and dual-axis visualizations.  
Create videos and enhance them with background music.

## Poster and Report
The proposal report：https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/Shilin_Ou_Final_Proposal.docx


Poster：[https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/docs/poster](https://github.com/STATS201-DKU-Autumn2024/Shilin_Ou_ProblemSet/blob/main/visualizations/Poster.png)
