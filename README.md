# Stock Price Prediction using NLP
This project aims to create a classifier to use news headlines and sentiment analysis in order to predict whether a stock's value increases or decreases. This project incorporates different NLP techniques as well as different ML algorithms in order to find the best fit.

## Data used
Dataset taken from: https://www.kaggle.com/competitions/stock-market-prediction-and-sentimental-analysis

The dataset consisted of 27 columns:
- One column consisting of the date
- One boolean column consisting of the label - 0 means the price decreases, 1 means the price increases
- 25 columns consisting of the top 25 headlines

## Data Cleaning and Vectorization
To clean the data, I have converted the headlines into lowercase, removed non-english characters and stopwords, and then performed stemming.

To vectorize, the following Natural Language Processing algorithms were used in this project:
- Bag of Words
- TF-IDF
- Word2Vec

## Predicting
The Machine Learning algorithms used for classification in this project are:
- Multinomial Naive Baye's Classifer
- LSTM RNN Classifier
- Random Forest Classifier

## Comparing the accuracy
I have compared the accuracy of different algorithms paired with different ML algorithms which can be seen below:

### Multinomial NB
- Bag of Words: 77.07%
- TF-IDF: 85.18%
- Word2Vec: MNB does not support negative values that Word2Vec might give. After using MinMaxScalar to normalize the values, an accuracy of 52.06% was achieved.

### Random Forest
- Bag of Words: 76.85%
- TF-IDF: 77.89%
- Word2Vec: 76.03%

### LSTM with Word Embedding
A deep learning approach with LSTM and Word Embedding layers was unable to produce an effective accuracy on the validation set even after trying different combinations of layers and different hyper parameters. It gave an accuracy of 53%.

The best accuracy was achieved with a combination of TF-IDF and Multinomial Naive-Bayes algorithms which was 85.18%.