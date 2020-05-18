# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & Classification

## Gabriel Choo, SG DSI 14

### Problem Statement

"Men are from mars, women are from venus"

As users from subreddit AskMen and AskWomen expresses themselves differently, how can we accurately differentiate them through the use of languages or words?

### Executive Summary

This report provides an inference and evaluation of the model through the use of various natural language processing technique to differentiate between reddit askmen and askwomen subreddits. Methods of inference includes detailed look at top features, confusion matrix, sensitivity, specificity, precison and ROC scores.

Results of model analysed shows that there are some common and frequent words used by the opposite sex. For AskMen's subreddit, words like 'men','girlfriend','girl','guy' are being used together to distinct the AskMen's post. Likewise, words like 'ladies','women','partner','feel' are amongst the words that differentiate AskWomen's post. Through the evaluation of precision, it shows that the model has correctly classified 77% of the 555 unseen subreddit posts.

The report finds the performance of the model not reaching it's full potential as there are signs of overfitting of training models. The area of weakness can be improved by collection of more datas for training of the model to drive the variance down. In addition, stop-words can be further refine by adding more helping verbs to reduce the number of features. Lastly, we can also consider to eliminate features with extremely low frequency.

It should be highlighted the fact that the project conducted has some limitations. Firstly, assumptions has been made that the majority of AskWomen's subreddit users is mostly women and Askmen's subreddit users is men. There might be instances that opposite sex can contribute to any of the subreddit and the posts has been taken to train the model.

### Data source:

- [Ask Men](https://www.reddit.com/r/AskMen/)
- [Ask Women](https://www.reddit.com/r/AskWomen/)

### Data Dictionary

|Feature|Type|Description|
|:---|:---|:---|
|**Subreddit**|*obj*|Specific online community and dedicated to a particular topic
|**Selftext**|*obj*|posts written by user
|**Title**|*obj*|title of the posts written by user
