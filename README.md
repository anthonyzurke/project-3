# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### Table of Contents

1. [Problem Statement](#Problem-Statement)
2. [Data Dictionary](#Data-Dictionary)
3. [Preprocessing & Modeling](#Preprocessing-&-Modeling)
4. [Conclusion and Recommendations](#Conclusion-&-Recommendations)

---

### Problem Statement

My company has partnered with a sports marketing agency to expand their market into college athletics. We have generated 2 models, a Logistic Regression Model, and Random Forest Classifier, using posts from r/CFB and r/CollegeBasketball on Reddit. We will gather the data from these models ot distinguish most commonly talked about topics and also, differentiating them to provide the most effective marketing strategies. 

---

### Data Dictionary
|Feature           |Type    |Dataset            |Description              |
|---               |---     |---                |---                      |
|subreddit         |int     |df_cfb & df_bball  |name of subreddit        |
|title             |object  |df_cfb & df_bball  |title of subreddit post 0: CFB 1: CollegeBasketball  |
|selftext          |object  |df_cfb & df_bball  |subtext of subreddit     |
|post              |object  |df                 |title + subtext          |
|post_length       |int     |df                 |engineered feature       |
|post_word_count   |int     |df                 |engineered feature       |
|stemmed_post      |object  |df                 |engineered feature       |
|lem_post          |object  |df                 |engineered feature       |

---

### Preprocessing & Modeling

This analysis examined 2,500 posts from both subreddits. Data extraction included scraping Reddit for the data. Data cleaning included dropping duplicated rows and null values. Hyperlinks and outliers were cleaned and dropped, respectfully. Using CountVectorizer I was able to identify the top 15 most common words used in each subreddit. To end the analysis the models used were Logistic Regression and Random Forest Classifier to determine with model would be more successful in predicting posts from the subreddits.

---

### Conclusion & Recommendations

Logistic Regression was able to predict posts with 77% accuracy and the Random Forest Classifier had an accuracy score 78%. the Random Forest Classifier also had a higher cross val score of .81 compared to the Logistic Regression cross val score of .79. 

I would recommend that sports marketing agency that has partnered with us to use the Random Forest Classifier to properly market towards their target market and to take advantage of the opportunities on recruiting websites. 

---