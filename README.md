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

- We 
 
 
# Neural Network
  
  - This model was created using tf.keras.models.Sequential, which defines a SEQUENCE of layers in the neural network. These sequence of layers used were the following:
  - One Embedding layer:  This is the process that help us to go from just a string of numbers representing words to actually get text sentiment. This process is     called embedding, with the idea being that words and associated words are clustered as vectors in a multi-dimensional space. 
  - One GlobalAveragePooling1D layer
  - Two Dense layers: This adds a layer of neurons. Each layer of neurons has an activation function to tell them what to do. Therefore, the first Dense layer       consisted in 24 neurons with relu as an activation function. The second, have 1 neuron and sigmoid as activation function. 

- We built this model using adam optimizer and binary_crossentropy as loss function, as we're classifying to different classes.

- The number of epochs=30

- We obtained Accuracy 0.8800 for the train data and Accuracy 0.8171 for the validation data.
  
 <p align="center">
  <img src="https://github.com/lilosa88/Sarcasm-detection/blob/main/Images/Screenshot%20from%202021-05-31%2016-10-14.png" width="320" height="460">
 </p>  
