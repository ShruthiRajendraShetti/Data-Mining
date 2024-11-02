# SEMMA (Sample, Explore, Modify, Model, Assess) methodology for tweet sentiment analysis 

SEMMA is a data mining framework primarily used for large-scale data analysis and focuses on a systematic approach to model building.

## 1. Sample
Objective: Select a representative sample of the dataset for analysis.
Action:
Since our dataset is already manageable in size, we can use the full dataset. However, for large-scale projects, we could sample a portion of the data to test the process before scaling.
Alternatively, if memory constraints apply, consider sampling a subset (e.g., 10-20%) of the data to begin with.
Let’s start with the Sample and Explore phases in code, analyzing the data distribution and basic text characteristics.

## 2. EXPLORE
Objective: Conduct exploratory data analysis (EDA) to understand the data structure, patterns, and potential issues.
Distribution Analysis: Examine the distribution of sentiment labels to identify any class imbalance.
Text Analysis: Analyze text length, word frequency, and common phrases to understand tweet characteristics.
Data Quality Checks: Identify and handle missing values, duplicates, or outliers in the text
The dataset contains 27,481 entries with 4 columns: textID, text, selected_text, and sentiment.
There is 1 missing value in the text column, which we’ll handle in the Modify phase.
Sentiment Distribution: The dataset has an imbalanced sentiment distribution, with more entries for the neutral class compared to positive and negative.

![output](https://github.com/user-attachments/assets/522628a8-5080-43d7-aafe-2dce2627bb31)


## 3. Modify
Steps in the Modify Phase:
Handle Missing Values: Remove any rows with missing values in the text column.
Text Cleaning: Clean the text by removing URLs, mentions, hashtags, punctuation, and converting to lowercase.
Encoding Sentiment Labels: Convert sentiment labels (positive, neutral, negative) to numerical values.
Feature Engineering:
TF-IDF Vectorization: Convert the cleaned text to numerical features.
Text Length Feature: Add a feature representing the character length of each tweet.

The following transformations are applied:

Missing Values: Rows with missing text values were removed.
Text Cleaning: URLs, mentions, hashtags, and punctuation were removed, and text was converted to lowercase.
Encoding: Sentiment labels were encoded into numerical values in the sentiment_encoded column.
Feature Engineering:
TF-IDF Vectorization: Transformed cleaned_text into a matrix of numerical features.
Text Length: Added text_length as an additional feature.
