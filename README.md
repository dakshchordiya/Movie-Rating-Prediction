# Movie-Rating-Prediction

## Table of contents
* [About the project](#About-the-project)
* [Sentiment Analysis](#Sentiment-Analysis)
* [Weighted Average of all reviews](#Weighted-Average-of-all-reviews)

### About the projec
* This project is a part of my internship at Reliance Jio. 
* The project intended to Predict an overall rating for a movie, considering all the reviews and ratings on various websites like IMDb, Rotten Tomatoes, Book My Show, etc.
* Every Movie Rating was Calculated based on a number of factors like the sentiments in the reviews, the frequency and importance of each user based on his ratings history, The demographic statistics of the users who rated the movie, and many more.
* The particular aim of the project was to come up with a formula for the weighted average of all the above mentioned factors and rate the movie based on those factors, such that it closely resembles the ratings of those websites.
* The Complete bundle of all the files used in the project can be found at https://drive.google.com/drive/folders/1HWUaIp6qesEq3OLbmgFRb9MaIuBH63d4?usp=sharing.
* The purpose of this repository is to present the main python codes used in the project.
* The following the are twparts of project completed thus far:
	
### Sentiment Analysis
* This folder contains different types of approaches to predict the sentiments of a user in his review. Each review can have a sentiment value between 1 and 10, with 10 being the best sentiment.
* As presented in various research papers, the state of the art model for sentiment analysis currently is the XLNet model, I tried to utilise the variations of that pretrained model(Also tried Bert) to predict the sentiments of the user.
* The Usage of various Code files is as follows:
  - Download Dataset.ipynb : Download the various datasets to be used.
  - Scraping Movie Reviews.ipynb : Scraping IMDb movie reviews and the ratings associated with the ratings of various movies.
  - Multi-Class Sentiment-regression-using-XLNet.ipynb : Treating the sentiment analysis as a regression task and predicting the rating associated with each review as a continuous value.
  - 08_sentiment_analysis_with_bert.ipynb : Uses the Bert pretrained model to predict the review among the following 3 categories : "Positive", "Negative", "Neutral".
  - Multi-class classification/Sentiment-classification-using-XLNet.ipynb : Treating the sentiment analysis as a binary Classification task and predicting the rating associated with each review as a binary value.
  -  Multi-class classification/5-Class Sentiment-classification-using-XLNet.ipynb : Treating the sentiment analysis as a 5-way Classification task and predicting the rating associated with each review among 1,2,3,4,5 values.
  -  Multi-class classification/10-Class Sentiment-classification-using-XLNet.ipynb : Treating the sentiment analysis as a 10-way Classification task and predicting the rating associated with each review among 1,2,3,4,5,6,7,8,9,10 values.
* The best performing Model among all these codes was "Multi-Class Sentiment-regression-using-XLNet.ipynb", which treats the problem as a regression task and predicts the rating as continuous values.

	
## Weighted Average of all reviews
