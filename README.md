# Knowledge Discovery in Databases (KDD) process for tweet sentiment analysis

Medium Article - https://medium.com/@shruthi.rajendrashetti/medium-article-analyzing-tweet-sentiment-with-the-kdd-process-1b1e39ff1055

## 1. Selection
Objective: Identify and select relevant data for sentiment analysis.
Action:
Use the original text, sentiment, and possibly selected_text columns as the primary inputs.
Ensure that only complete records are selected by removing rows with missing values in these key columns.

## 2. Preprocessing
Objective: Clean and prepare the text data, removing noise and ensuring quality.
Steps:
Text Cleaning: Similar to CRISP-DM, apply text cleaning (removing URLs, mentions, punctuation, and special characters).
Handling Missing Values: Remove or fill any remaining missing values in the text and sentiment columns.

## 3. Transformation
Objective: Convert the cleaned data into a format suitable for machine learning.
Steps:
Encoding: Encode the sentiment labels into numerical values.
Feature Engineering: Use techniques like TF-IDF to create vectorized representations of the text.
Scaling: Scale any additional features (e.g., text length) if necessary.

## 4. Data Mining
Objective: Apply machine learning models to classify tweet sentiments.
Model Choices:
Use a baseline model, such as Logistic Regression or Support Vector Machine, to classify tweets as positive, negative, or neutral.
Hyperparameter Tuning: Optimize the model by tuning parameters (e.g., regularization strength for Logistic Regression, kernel choice for SVM).

Train-Test Split: Split the dataset into training and testing sets.
Model Training: Train a Logistic Regression model on the TF-IDF features and any additional features.
Evaluation: Evaluate the model’s performance using metrics like accuracy, precision, recall, and F1-score.

## 5. Interpretation/Evaluation
Objective: Evaluate and interpret the results to ensure they align with the original goals.
Metrics:
Use metrics such as accuracy, precision, recall, and F1-score.
Insights:
Highlight strengths and limitations, especially how well the model performs across different sentiment classes.

The Logistic Regression model has been trained, and here are the results:

Accuracy: 67.9%
Precision, Recall, and F1-Scores:
Negative: F1-score of 0.62
Neutral: F1-score of 0.67
Positive: F1-score of 0.74
The model performs best on the positive sentiment, while negative is slightly weaker, possibly due to class imbalance.
