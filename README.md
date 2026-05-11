# Social Media Sentiment Analysis and Engagement Prediction

This project analyzes social media posts to understand sentiment patterns, platform differences, hashtag trends, geographic variation, and user engagement behavior. It was completed as part of the NYU Tandon Data Science Bootcamp.

## Project Overview

The goal of this project is to explore how sentiment in social media content relates to user engagement metrics such as likes and retweets. The project includes data cleaning, exploratory data analysis, visualization, sentiment classification, statistical hypothesis testing, and baseline engagement prediction.

The dataset contains text posts, sentiment labels, timestamps, platforms, hashtags, likes, retweets, and country information.

## Objectives

- Analyze the distribution of sentiment categories across social media posts.
- Compare sentiment patterns across different platforms.
- Explore temporal trends in sentiment over time.
- Examine relationships between sentiment and engagement metrics.
- Identify common hashtag and geographic patterns.
- Build baseline machine learning models for sentiment classification.
- Explore engagement prediction using sentiment, platform, and hashtag features.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- scikit-learn
- SciPy
- Jupyter Notebook

## Dataset

The project uses a social media sentiment dataset with the following types of features:

- Text content
- Sentiment labels
- Platform
- Timestamp
- Hashtags
- Likes
- Retweets
- Country

The cleaned dataset removes unnecessary columns, trims inconsistent categorical values, and prepares text data for analysis and modeling.

## Project Workflow

### 1. Data Cleaning

The dataset was cleaned by:

- Removing unnecessary `Unnamed` columns.
- Trimming extra whitespace from categorical fields.
- Cleaning text content for NLP analysis.
- Converting engagement metrics such as likes and retweets into numeric values.
- Creating a cleaned text column for modeling.

### 2. Exploratory Data Analysis

EDA was performed to understand:

- Overall sentiment distribution.
- Platform distribution.
- Sentiment trends over time.
- Average likes and retweets by sentiment.
- Hashtag patterns.
- Geographic sentiment differences.

### 3. Sentiment Classification

Baseline NLP models were trained using TF-IDF features:

- TF-IDF + Logistic Regression
- TF-IDF + Linear SVM

The models were evaluated using classification metrics such as accuracy, macro-F1 score, and classification reports. Linear SVM performed better among the baseline models.

### 4. Statistical Hypothesis Testing

Several statistical tests were conducted:

- Chi-square test for sentiment distribution across platforms.
- Kruskal-Wallis test for engagement differences across sentiment categories.
- Chi-square test for sentiment distribution across countries.

The results were interpreted carefully because the dataset is relatively small and some sentiment-country combinations have sparse sample counts.

### 5. Engagement Prediction

Random Forest Regression models were used to explore whether sentiment, platform, and hashtag features could help predict engagement metrics such as likes and retweets.

This part of the project was exploratory. Engagement is influenced by many external factors not included in the dataset, such as follower count, posting time, account popularity, and trending events.

## Key Findings

- Sentiment categories show different engagement patterns.
- Platform differences appear to influence likes and retweets.
- Hashtag usage may be related to higher visibility and engagement.
- Linear SVM performed better than Logistic Regression for baseline sentiment classification.
- Random Forest models showed limited but useful predictive signals for engagement prediction.
- Statistical tests suggest possible relationships between sentiment, platform, geography, and engagement, but results should be interpreted as exploratory rather than causal.

## Limitations

- The dataset is relatively small.
- Some sentiment labels have very few samples.
- Sentiment categories may be noisy or ambiguous.
- Engagement depends on external factors not included in the dataset.
- Chi-square tests may be affected by sparse category combinations.
- The models are baseline models and are not production-level NLP systems.

## Future Improvements

- Use larger and more balanced social media datasets.
- Apply advanced text embeddings such as BERT or RoBERTa.
- Add user-level features such as follower count and posting time.
- Perform topic modeling to better understand content themes.
- Improve engagement prediction with richer features.
- Explore causal analysis to distinguish correlation from causation.

## Files

```text
final_project.ipynb                   # Main notebook with data cleaning, EDA, modeling, and analysis
sentimentdataset.csv                  # Raw dataset
df_clean.csv                          # Cleaned dataset
sentiment_analysis_ppt.pptx           # Final project presentation
