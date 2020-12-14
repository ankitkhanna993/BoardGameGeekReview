# BoardGameGeekReview

## Introduction

In the given data, provided and owned by the wonderful people at BoardGameGeek, the world’s largest board game site, it contains all the comments and reviews by the users of all the board games.


## Goal

Given the review of any game, we predict the rating for that review.

In this notebook, we explore a dataset containing reviews of various board-games and their respective ratings.
With this, we build a predictor that would obtain scores from given review.

## Data Description

The orginal Board game data is vast (1GB-1,31,70,073 rows data for review file) and time consuming process to clean, that needs excellent memory of the computer. So to avoid complexity this project has taken 30,000 unbalnced and 20,000 balanced data set for the aanalysis and model development. The file contains
1. GameID
2. Rating
3. Comment

## Multinomial Naive Bayes

Multinominal Naive Bayes (MNB) algorithm has been widely used in text classification due to its computational advantage and simplicity. MNB maximizes likelihood rather than conditional likelihood or accuracy. The task of text classification can be approached from a Bayesian learning perspective, which assumes that the word distributions in documents are generated by a specific parametric model, and the parameters can be estimated from the training data.

## Support Vector Machine

The objective of a Linear SVC (Support Vector Classifier) is to fit to the data, returning a "best fit" hyperplane that divides, or categorizes the training data.After getting the hyperplane, then the model can be feeded with test sample to classify the "predicted" class.

## K-Nearest Neighbour

K-nearest neighbors (KNN) algorithm is a type of supervised ML algorithm which can be used for both classification as well as regression predictive problems. K-nearest neighbors (KNN) algorithm uses ‘feature similarity’ to predict the values of new datapoints which further means that the new data point will be assigned a value based on how closely it matches the points in the training set.

## Data Cleaning/Pre-processing

1. All text is initially lowercased and punctuation is removed in conjuction to it.
2. A list of stopwords is extraced from the NLTK corpus and additional stopwords are appended to it.
3. Stopwords are then removed from the dataset and a cleaned data column is created.
4. Lemmatization was not made a part as reviews were in multiple language, which would have further lowered the score.

## NLP Technique Used

### CountVectorizer

1. We used CountVectorizer which we realized had already used many of the data cleaning methodologies that weren’t necessary to be built in the first place.
2. It Built a sparse matrices of extremely high dimensional data with ease and not consuming too much RAM
3. We picked 10000 features to build the multinomial model with.
4. Tried to get help with its given documentation by scikit learn.org

### File Execution
Download and run the jupyter notebook.
