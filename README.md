# CRISP-DM

# A. Business Understanding Phase for Tweet Sentiment Analysis

1. Project Objective
The goal of this project is to classify tweets by their sentiment, identifying each tweet as either positive, negative, or neutral.
This analysis will enable businesses, social media platforms, or researchers to gain insights into public sentiment, customer satisfaction, and trending opinions on specific topics.

2. Business Goals
Sentiment Monitoring: Use sentiment classification to monitor public sentiment on various topics, including products, events, and brand perception.
Customer Satisfaction: By analyzing customer feedback, companies can identify issues, adjust their strategies, and improve user engagement and customer satisfaction.
Market Research and Trend Analysis: Understand public opinion on new products, services, and trending topics, which can help in shaping marketing campaigns and improving product offerings.

3. Success Criteria
Accuracy of Sentiment Prediction: A high level of accuracy (e.g., above 80%) for sentiment classification is a key success metric.
Consistency Across Sentiment Types: The model should perform consistently well across positive, negative, and neutral classes, with special attention to the smaller classes.
Actionable Insights: The model’s predictions should lead to actionable business insights, like highlighting frequent customer concerns or identifying trending topics.

4. Key Assumptions and Constraints
Assumptions:
Tweets reflect genuine user sentiment.
Each tweet's sentiment can be reliably classified as positive, negative, or neutral.
Constraints:
Class Imbalance: Some sentiment classes may be underrepresented, which could affect model performance.
Tweet Length and Language: Short tweet lengths, abbreviations, and slang may limit the model's understanding.
Real-Time Application: For real-time sentiment analysis, the model may need optimization to handle a large volume of tweets efficiently.

5. Risks
Data Quality: Noise in tweets (e.g., abbreviations, emojis) may impact the model’s accuracy.
Changing Language Patterns: Slang and sentiment expressions evolve over time, requiring periodic model retraining.
Bias: Potential bias in the dataset may lead to inaccurate predictions, especially for underrepresented topics or groups.

# B. Data Understanding Phase
From the initial exploration:

The dataset has 27,481 rows and 4 columns:
textID: Unique identifier for each tweet.
text: Full text of the tweet.
selected_text: Extracted portion of the tweet that reflects the sentiment.
sentiment: Overall sentiment label of the tweet (neutral, positive, or negative).
There is one missing entry in the text and selected_text columns.
Sentiment distribution is worth examining to understand class balance.

Distribution Of Sentiment Classes
Insights from Data Understanding
Sentiment Distribution:

The dataset shows an imbalanced distribution of sentiments, with neutral being the most frequent class, followed by negative and positive.
Text Length:
The average length of a tweet (text_length) is around 68 characters, while the average length of the selected_text is 37 characters.
Some tweets are as short as 3 characters, and some reach the Twitter limit of 141 characters, which is useful for model selection and feature engineering.
These insights suggest that:

We might need to address the class imbalance during the modeling phase.
Feature engineering may include text length as a feature to potentially improve model performance.

# C. Data Preparation Phase for Tweet Sentiment Analysis
In this phase, we’ll prepare the cleaned dataset for modeling by addressing any remaining issues and transforming it into a format suitable for machine learning.

1. Handling Missing Values
Action: Since text and selected_text columns have one missing value each, we’ll remove these rows or fill them if necessary.
Rationale: Missing values in text data can interfere with model training.

2. Encoding Sentiment Labels
Action: Convert the sentiment labels (positive, negative, neutral) into numerical format for model compatibility. This can be done through label encoding:
positive = 1
neutral = 0
negative = -1
Rationale: Encoding helps the model interpret categorical labels in numerical form.

3. Feature Engineering
Text Length: Use text_length and selected_text_length as potential features, as longer tweets may carry different sentiment than shorter ones.
TF-IDF Vectors: Transform the cleaned_text column into numerical representations using TF-IDF (Term Frequency-Inverse Document Frequency). This method gives weight to important words in each tweet based on their frequency across the dataset.
Rationale: These features provide numerical input for models and help capture important aspects of tweet content.

4. Splitting the Data
Action: Split the dataset into training and test sets, typically with a 70-80% training and 20-30% test ratio.
Rationale: This split allows us to train the model and then validate it on unseen data to gauge generalization.

5. Standardization and Scaling
Action: Scale the text_length and selected_text_length features, if used, to bring them to a similar scale, typically using standardization (z-score normalization).
Rationale: Scaling helps prevent certain features from dominating others due to their range, improving model performance.

# D. MODELING
In the Modeling Phase, we’ll select and train a model suitable for sentiment classification. Since this is a multiclass classification task, we can start with a few baseline models and compare their performance. I’ll begin by implementing a Logistic Regression model as a baseline and evaluate its performance. 

Steps:
Train a Logistic Regression Model.
Evaluate the Model on the test set using accuracy, precision, recall, and F1-score.
Compare Results and adjust as needed.
Let’s proceed with this approach.

Model Performance
The Logistic Regression model achieved:

Accuracy: 67.9%
Precision, Recall, F1-score:
Negative: F1-score of 0.62
Neutral: F1-score of 0.68
Positive: F1-score of 0.74
The model performs best on the positive class, with lower performance on the negative class, likely due to class imbalance and language complexity.

# E. Evaluation Phase for Tweet Sentiment Analysis
In the Evaluation Phase, we’ll assess the model's performance and interpret its practical utility. Here’s how we’ll approach this:

1. Performance Metrics Review
Accuracy: 67.9%, indicating that the model correctly predicts sentiment for nearly 68% of the test tweets.
Precision, Recall, and F1-Score: These scores vary across the three classes (negative, neutral, positive). The F1-score provides a balanced measure of precision and recall, helping evaluate each class’s performance:
Positive sentiment performed best (F1-score: 0.74), suggesting the model can reliably detect positive sentiments.
Neutral sentiment also showed solid performance (F1-score: 0.68), while negative was slightly weaker (F1-score: 0.62), likely due to data imbalance.

2. Model Interpretation
Strengths:
Good performance on positive and neutral sentiments.
Logistic Regression’s interpretability helps identify influential words or phrases impacting predictions.
Limitations:
Lower performance on negative sentiment might miss critical user concerns.
Logistic Regression may not capture complex patterns, potentially limiting its effectiveness for nuanced language.

3. Potential Improvements
Class Balancing Techniques: Use techniques like oversampling or weighted loss to address the imbalance in classes.
Advanced Model Exploration: A more complex model (e.g., Support Vector Machine or Random Forest) could capture subtler nuances.
Feature Engineering: Experiment with n-grams or embeddings (like Word2Vec or BERT) to enrich feature representation.
