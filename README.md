# Project 3: Reddit Classification


## Executive Summary


Since its founding in 1990, IMDB.com has been the No.1 internet movie database which is written solely by contributors in the internet community. 

With daily submissions on the rise, much of the data on the website is still being handled by humans. Many of the errors stem from incorrect genres and has led to IMDB's customers not being able to find or link up with the appropriate content.


To improve, IMDB is looking to invest in a classifier to help auto-populate content such as the genre of a movie in the submission entries to keep its database relevant and clean. 
As an exploratory study into whether IMDB should invest in this upgrade, a team of Data Engineers are tasked to see if it is possible to accurately identify a movie genre based on the movie plot. 


The data for this project was drawn from /r/scifimovies and /r/HorrorMovies, two movie subreddit groups who discuss and share plots, reviews and searches for the genre titles.


Using a MultinomialNB classifer, we are able to accurately predict a Sci-fi or Horror post solely from key words from the plot entry on reddit. 


In the case for IMDB, this exploratory study has been successful for these two genres and the study should continue to expand to more genres to see if machine learning is capable of handling and differentiating accurately between more classes. 

If done well, this will benefit not just IMDB's source credibility, it will also improve the UX of the site and could possibly branch into improving other types of content in the site.

---- 

## Contents:

- 1.0 Data Collection and Cleaning
- 2.0 EDA & Data Preprocessing
- 3.0 Model Building
- 4.0 Reddit Classification Report


----

## Conclusion and Recommendations¶

As a exploratory study into whether IMDB should invest in an upgrade, a team of Data Engineers are tasked to see if it is possible to accurately identify a movie genre based on the movie plot.

In order to answer our problem statement, we have:

1. Taken raw data from two subreddits /r/scifimovies and /r/HorrorMovies
2. Built a function with a sleeper to retrieve data from Reddit's API
3. Cleaned and explored our data
4. Further processed our data by normalizing using varous techniques.
5. Split the data into test and training sets
6. Tested different variations of our models to get the highest scoring model
7. Fitted and optimized the final model to achieve a ROC_AUC score of 0.9577


Although our final score did not beat the score of the intial model, the optimized model has manage to minimise overfitting by scoring better than its best score. This means given unseen data on Horror and Sci-fi, our model will be able to perform well.

In the case for IMDB, this exploratory study has been successful for these two genres and should continue to expand to more genres to see if machine learning is capable of handling and differentiating accurately between more classes. If done well, this will benefit not just IMDB's source credibility, it will also improve the UX of the site and could possibly branch into improving other types of content in the site.

As data on reddit forums does seem quite limited on movie information, it is advisable to look for other soures of data (e.g rotten tomatoes, IMDB's own database) to harness potentially better data for more accurate predictions.

---- 

### Data Dictionary :

|Feature|Type|Dataset|Description|
|---|---|---|---|
|stemmed|object|stem_data/cvec_x_data/tvec_x_data|Data: concatenated Reddit post (title, selftext)| 
|label|int|stem_data/cvec_x_data/tvec_x_data|label: 1 for Sci-fi, 0 for Horror| 


----

Sources:
    
Watson, A. (2020, January 10). Movie releases in North America from 2000-2019. Retrieved June 25, 2020, from https://www.statista.com/statistics/187122/movie-releases-in-north-america-since-2001/<br>

IMDB - contributors. (n.d.). Retrieved June 25, 2020, from https://contribute.imdb.com/czone?ref_=nv_cm_cz<br>

Bitext. (n.d.). What is the difference between stemming and lemmatization? Retrieved June 25, 2020, from https://blog.bitext.com/what-is-the-difference-between-stemming-and-lemmatization/<br>

Brownlee, J. (2020, January 14). ROC Curves and Precision-Recall Curves for Imbalanced Classification. Retrieved June 25, 2020, from https://machinelearningmastery.com/roc-curves-and-precision-recall-curves-for-imbalanced-classification/<br>

Markham, K. (2020, February 03). Simple guide to confusion matrix terminology. Retrieved June 25, 2020, from https://www.dataschool.io/simple-guide-to-confusion-matrix-terminology/<br>
