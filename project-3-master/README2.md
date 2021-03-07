Problem Statement:

Not exactly a problem in itself, but the goal of the project was to build a model that could accuratly classify what subreddit a title of a post came from. Accurate would mean above the null.

Executive Summary:

I scraped two subreddits, Boxing and MMA, trying to find a difference. I did this by using the push shift api.
The scraped data had some characters that werent useful in classification and confused the models a bit, so i removed stop words, and lemmatized.
The eda revealed some similar words that were in common, but also revealed that a major deciding factor were the names of different fighters to their respective disciplines
The models i ran were six in total

CountVectorizer with:
LR
NB
KNN

and 

TFIDF with:
LR
NB
KNN

Where four resulted in the best scores around 88 after some parameter tuning
The only real reccomendation i can make from this is if the subreddits ever want to further distinguish themselves, i would tell them to increase discussion on their individual disciplines such as technique.


There are 6 notebooks that show the entire data process:
The two api pulls (APIFetch)
Cleaning the data (Cleaning)
Exploratory Data Analysis (EDA)
Modeling (Modeling)

Conclusions:

I actually did modeling without cleaning the original data, and the scores remained about the same. It seems like for these specific subreddits, what the models use work but what they cant use cant really be improved. This probably comes from the similar words, as they are both combot sport communities.