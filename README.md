# Predicting Bitcoin

The project is to predict the price of Bitcoin. First, we sourced the data on Kaggle.com which provided us with tweets from @BTCTN, Official Twitter account for http://news.bitcoin.com. Then created a predictive model using the Random Forest Regressor model. After, we fit a Deep neural network model to the data and compared the performance of both models to determine which has sufficient predictive power. In addition to the above, used the Sentiment Analyser, Named Entity Analysis (NER) and Word cloud to carry out text analysis on the data.

# Motivation

Bitcoin is important to our financial future, our intent is to demonstrate that just like Gold, Bitcoin is also a store of value, with price driven by sentiment, market demand and supply.

# Libraries

Collaborated using Google Collab, Imported the following libraries:
* Pandas
* Numpy
* NLTK
* SKLearn
* Matplotlib
* Spacy

# Data Clean up

* Read csv
* Merged tweets using lambda function
* Renamed columns 
* Output was two btc_revised dataframes
* Merged dataframes 
* Checked for nulls and duplicates
* Dropped columns 
* Output was a final dataframe ‘df’

# Sentiment Analysis

## Run sentiment analysis on the final dataframe 
### Result:

* Generally positive sentiment about Bitcoin on average 
* Standard deviation, min, max numbers shows the high volatility characteristic of Bitcoin itself.  

# Model 1 - Random Forest Regression Model 
## Random Forest Regression Model

* Tree based algorithm that samples data and builds several smaller decision trees which combined create a strong classifier (ensemble learning). 
* RFR is very robust against overfitting and can be used with various types of data.
* Used to rank importance of input variables in a natural way
* Can handle thousands of input variables without variable deletion 
* Robust to outliers and non-linear data
* Can be used on large databases. 

# Model Summary & Evaluation

## Summary

* Outlined useful features in the cleaned-up data
* Split into Training and Testing sets
* Created a dataframe to store model performance
* Determined best parameters for the ML model using defined function 
* Fit data into model 
* Make predictions

## Evaluation

* Evaluated this model performance using the balanced accuracy score and mean squared error. 
* The accuracy score of 0.29 shows that the model is 30% accurate at predicting the price of Bitcoin. We believe this is due to limited data.
* Though based on the research, it was found out that in many cases despite the lower r2 score the model performance was still considered good.

# Model 2 – LSTM RNN (Long short-term memory Recurrent Neural network) 

* Deep learning model, also very good at modelling sequence data. 
* Intention is to compare with Random Forest Regressor Model for accuracy in predicting Bitcoin 

## Steps

* Window size = 20
* Train, test and split
* Scale Data using MinMaxScaler
* Reshape data features
* Compiled Sequential model +dropout
* Fit model into training data
* Make predictions

## Evaluation

* Evaluated this model performance using the mean squared error below
* The score of 0.006 shows that the model error is very low which is good.
* Attempted to improve the performance of this model by reducing the number of feature column. Number of layers and dropout was retained.
### Result : Mean squared error increased to 0.08 and predictions flattened.


