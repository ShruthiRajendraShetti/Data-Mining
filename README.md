# SEMMA (Sample, Explore, Modify, Model, Assess) methodology for tweet sentiment analysis 

SEMMA is a data mining framework primarily used for large-scale data analysis and focuses on a systematic approach to model building.

## 1. Sample
Objective: Select a representative sample of the dataset for analysis.
Action:
Since our dataset is already manageable in size, we can use the full dataset. However, for large-scale projects, we could sample a portion of the data to test the process before scaling.
Alternatively, if memory constraints apply, consider sampling a subset (e.g., 10-20%) of the data to begin with.
Let’s start with the Sample and Explore phases in code, analyzing the data distribution and basic text characteristics.

### Distribution Of Sentiment Classes : 
The dataset contains 27,481 entries with 4 columns: textID, text, selected_text, and sentiment.
There is 1 missing value in the text column, which we’ll handle in the Modify phase.
Sentiment Distribution:
The dataset has an imbalanced sentiment distribution, with more entries for the neutral class compared to positive and negative.
