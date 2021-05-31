# Fake-News-Classifier
# Objective

- This project belongs to [kaggle's competitions](https://www.kaggle.com/c/fake-news/data). The objective is to sevelop a machine learning or Deep Learning program to identify when an article might be fake news.


# Code and Resources Used

- **Phyton Version:** 3.0
- **Packages:** pandas, numpy, sklearn, re, nltk, json, keras, tensorflow

# Data description

- A full training dataset with the following attributes:

  - id: unique id for a news article
  - title: the title of a news article
  - author: author of the news article
  - text: the text of the article; could be incomplete
  - label: a label that marks the article as potentially unreliable
    - 1: unreliable
    - 0: reliable

# Preprocessing

- We remove all the missing values.
- We clean the data by removing punctuations, stopwords and applying lowercase. Thus we use PorterStemmer, stemming is the process of reducing words to their       word stem.
 
 
# Models

- First model: Bag of words and Machine Learning model 
  - We apply the method of bag of words to the text.
  - We define the independent and dependent variables.
  - We do train and test split.
  - We apply MultinomialNB Algorithm
    - Train MultinomialNB Algorithm's Accuracy: 0.924
    - Test MultinomialNB Algorithm's Accuracy: 0.901

- Second model: One hot representation and Neural Network with LSTM
  - We apply one hot representation to the words in the text.
  - We apply padding to have the same lenght.
  - We apply the Neural Network model
    - This is composed by: One embedding layer, one LSTM layer, and one Dense layer with one neuron and sigmoid as activation function.
    - The Adam optimizer is used and the binary_croosentropy for loss.
    - Train Neural Network's Accuracy: 0.996
    - Test Neural Network's Accuracy: 0.906

- Third model: One hot representation and Neural Network with a Bidirectional LSTM and a Dropout layer
  - We apply one hot representation to the words in the text.
  - We apply padding to have the same lenght.
  - We apply the Neural Network model
    - This is composed by: One embedding layer, one Bidirectional LSTM layer, oNe Dropout layer and one Dense layer with one neuron and sigmoid as activation           function.
    - The Adam optimizer is used and the binary_croosentropy for loss.
    - Train Neural Network's Accuracy: 0.996
    - Test Neural Network's Accuracy: 0.907

- Fourth model: TF-idf Vectorizer and Machine Learning model 
  - We apply the method of TF-idf Vectorizer to the text.
  - We define the independent and dependent variables.
  - We do train and test split.
  - We apply MultinomialNB Algorithm
    - Train MultinomialNB Algorithm's Accuracy: 0.918
    - Test MultinomialNB Algorithm's Accuracy: 0.880
