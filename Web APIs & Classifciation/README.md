# Project 3: Web APIs & Classification

General Assembly DSI 19 Project 3 Adrian Teng 

## Project Introduction

1. Using Reddit's API to collect posts from two subreddits of your choosing.
2. NLP to train a classifier on which subreddit a given post came from. This is a binary classification problem.

## Problem Statement

We  hypothesis that by having two similar text-driven subreddits, as NLP will have a difficult time spotting the difference between the 2 subreddits. As there are over 1.5 million subreddits on reddit, we will be be classifying post from two subreddits that are heavily text driven, 'tifu' and 'confessions' respectively. 

We will be creating and comparing models: a logistic regression, a multinomial naive Bayes, a KNeighborsClassifier. The results obtained may be useful for reddit user who wants to submit his new post in the most optimal subreddit, so that he can attract more 'Upvotes' and 'Total rewards'.



## Executive Summary

In this project, it is splitted into three parts respectively:
- API & EDA (01_api_eda)
- Processing & Modeling (02_processing_modeling)
- Conclusion (03_conclusion)

In the first notebook, 01_api_eda, data was scrapped from Reddit. After gathering the raw data from the Reddit, exploration was done and new dataframe was created to better match the selection of models. Data cleaning was done, and duplicates was removed to strengthen the effectiveness of the project. At the end, TfidVectorizer and Logistic Regression was decided, based on their accuracy result.

In the second notebook, 02_processing_modeling, chosen subreddits was to pre-process. Regex Regular Expression Techniques was used to tokenize each post and title. Next, vectors of Stemmed and Lemmatized words from the tokens was created. GridSearch will be run across all classification models to rule out non-viable options. 

Classification models: Multinomial Naive Bayes, K-Nearest Neighbors and Logistic Regression will be used for accessment with the pre-processed data. They are also tested using two-vectorization transformers: CountVectorizer and TfidfVectorizer.

In the third notebook, 03_conclusion, unseen data was used to test against the selected models and further evaluted with the distribution of True positive, False Positive, False Negative and True Negative Preidtions. Additional features like, Accuaracy, Sensitivity, Specificity and Precision also put into actions.

Feature Analysis was done to support problem statement in the conclusion


## Conclusion 

- 1. Model 2 (TFIDF Logistic Regression) have the highest test score for both test and unseen test, as compared to the other models as a sucess metric in comparing text of two similar subreddits.

- 2. The similarity of the two subreddits is very high, from the feature analysis we can see that the top 20 words that overlapped is more than 70%.

- 3. Other than the test score, the overall Sensistivity, Specificity, Precicion are higher than Model 1(CV MultinomialNB).

- 4. Hence, if the post is so similar, Reddit user can consider posting in 'TIFU' instead of 'Confessions' to attract more viewers.
