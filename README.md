# Movie-Rating-Prediction

## Table of contents
* [About the project](#About-the-project)
* [Sentiment Analysis](#Sentiment-Analysis)
* [Weighted Average of all reviews](#Weighted-Average-of-all-reviews)

### About the project
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
  - [Download Dataset.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/Download%20Dataset.ipynb) : Download the various datasets to be used.
  - [Scraping Movie Reviews.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/Scraping%20Movie%20Reviews.ipynb) : Scraping IMDb movie reviews and the ratings associated with the ratings of various movies.
  - [Multi-Class Sentiment-regression-using-XLNet.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/Multi-Class%20Sentiment-regression-using-XLNet.ipynb) : Treating the sentiment analysis as a regression task and predicting the rating associated with each review as a continuous value.
  - [08_sentiment_analysis_with_bert.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/08_sentiment_analysis_with_bert.ipynb) : Uses the Bert pretrained model to predict the review among the following 3 categories : "Positive", "Negative", "Neutral".
  - [Multi-class classification/Sentiment-classification-using-XLNet.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/Multi-class%20classification/Sentiment-classification-using-XLNet.ipynb) : Treating the sentiment analysis as a binary Classification task and predicting the rating associated with each review as a binary value.
  -  [Multi-class classification/5-Class Sentiment-classification-using-XLNet.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/Multi-class%20classification/5-Class%20Sentiment-classification-using-XLNet.ipynb) : Treating the sentiment analysis as a 5-way Classification task and predicting the rating associated with each review among 1,2,3,4,5 values.
  -  [Multi-class classification/10-Class Sentiment-classification-using-XLNet.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/Multi-class%20classification/10-Class%20Sentiment-classification-using-XLNet.ipynb) : Treating the sentiment analysis as a 10-way Classification task and predicting the rating associated with each review among 1,2,3,4,5,6,7,8,9,10 values.
* The best performing Model among all these codes was "[Multi-Class Sentiment-regression-using-XLNet.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Sentiment%20Analysis/Multi-Class%20Sentiment-regression-using-XLNet.ipynb)", which treats the problem as a regression task and predicts the rating as continuous values.

	
### Weighted Average of all reviews
* This folder contains the code to scrape the data for reviews and all the other factors involved in getting the weighted average of ratings of al movies from IMDb, running the sentiments analysis model on the reviews to predict the rating associated with that review, and then finally using all the combined processed data of all users for a movie to predicts its final rating.
* The final input to the model would be an multi-dimensional array of the processed data of all the users to get a final rating of each movie.
* The Usage of various Code files is as follows:
	- [Scraping Movie Reviews.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Movie%20Reviews%20Weighted%20Average/Scraping%20Movie%20Reviews.ipynb) :This code helps in scraping all the data available for each movie from the IMDb website that factors in the final rating of a movie.
	- [Review Rating.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Movie%20Reviews%20Weighted%20Average/Review%20Rating.ipynb) : This code Runs the Sentiment analysis from the XLNet model from the previous step to rate the movie from each review.
	- [Reviews average.ipynb](https://github.com/dakshchordiya/Movie-Rating-Prediction/blob/main/Movie%20Reviews%20Weighted%20Average/Reviews%20average.ipynbb) : This code finally takes the input array of the complete processed data, run it on a model an predicts a final rating for each movie, that closely resembles the final IMDb rating of each movie.
 
