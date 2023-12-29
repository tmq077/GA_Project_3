# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: A self-help tool for couples to understand their attachment style

### Problem Statement

Comparing between 2018-2022 and 2013-2017, there has been a 4.6% drop in annual average marriage registered. In the last 10 years, average crude divorce rate is at 1.9 per thousand population. It was also reported that more couples, especially those recently married, are getting divorce. 

The recent trends in declining number of marriages and earliers divorces are a cause for concern. And communication is cited as one common reason for divorce. A strong and lasting relationship requires healthy communications. And the way we communicate with one another is influenced by our attachment styles. 

The objective of our project is to develop a tool which users can use to recognise and understand both theirs and their partner's attachment style. Attachment styles can be flexible and evolve over time with self-awareness and personal growth. Recognizing each other's attachment style and working on developing communication strategies can be beneficial for building healthier and more satisfying relationships.

---

### Data Used

Source: Reddit 
* [`Anxious Attachment Subreddit`](https://www.reddit.com/r/AnxiousAttachment/): A subreddit for individuals with anxious attachment style to learn more about the style, share experiences and find support.
* [`Avoidant Attachment Subreddit`](https://www.reddit.com/r/AvoidantAttachment/): A subreddit about and for individuals with avoidant atatchment style.

---

### Data Dictionary

|Feature|Type|Description|
|---|---|---|
|**subreddit**|*string*|AvoidantAttachment<br>AnxiousAttachment|
|**class**|*integer*|Class 0: Avoidant<br>Class 1: Anxious|
|**text_final**|*string*|Title of the subreddit post after cleaning and pre-processing|

---

### Notebook description

* [`01_webscraping`](/code/01_webscraping.ipynb): Data scraped from the respective subreddits using PRAW
* [`02_clean_eda_modelling`](/code/02_clean_eda_modelling.ipynb): Data preprocessing, exploring and visualizing the data and modeling. 

---

### Conclusion

- Our classifier model, Logistic Regression with Count Vectorizer, is able to classify individuals as either anxious or avoidant attachment style with 0.9 accuracy. 
- With this classifier model, we developed an easy-to-use self-help tool (https://attachment-style-classifier.streamlit.app/) to help couples identify their attachment styles. 
- Information and recommendations are provided based on the attachment style for couples to improve on communicating with each other. 

---

### Recommendations

#### Phase 1 - First release of the app on:
- MSF website
- MSF’s Telegram channel (i.e.,MSFCares)
#### Phase 2 - Improve accuracy of classifier model to ≥0.95 through:
- collecting more data from other similar subreddits
- exploring ways to tune the existing classifier model
- exploring the use of other classifier models (e.g., XGBoost) 
#### Phase 3 - Second release of the app with:
- expanded coverage of the other two attachment styles
