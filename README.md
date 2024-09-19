# Sentiment Analysis on Tweets using CNN and VGG-16
## Overview
This project focuses on sentiment analysis of tweets using the Sentiment140 dataset. We have developed and compared three convolutional neural network (CNN) models to classify tweets into two categories:

0: Negative Sentiment
1: Positive Sentiment
We leverage word embeddings from a pre-trained FastText model, each with an embedding dimension of 300, and apply these to CNN architectures for classification. Additionally, a VGG-16 based model is also trained for comparison.
## Dataset
The [Sentiment140](https://www.kaggle.com/datasets/kazanova/sentiment140) dataset contains 1.6 million tweets, but for the purposes of this project, we use a subset of 130,000 tweets for both training and testing.
## Preprocessing
Removal of stop words, digits, special characters, and punctuation.
Tweets are tokenized into words, and each word is represented by its FastText embedding (300-dimensional vector).
## Models
**1. First CNN Model**
Architecture:

- Convolutional layers with kernel sizes of 2, 3, and 5.
- 265 filters in each layer.
- Batch normalization and global max-pooling layers.
- Dense layer with a sigmoid activation function for binary classification.
- Input size: sequences of word embeddings with a fixed length of 18 and dimensionality of 300.
Performance:

- Accuracy: 73%
- Precision:
   Negative: 0.72
   
   Positive: 0.75
- Recall:
   Negative: 0.76
   
   Positive: 0.71
   
**2. Second CNN Model:**
Architecture:

- Convolutional layers with varying kernel sizes of 2, 4, 6, and 10.
- Number of filters: 64, 128, and 265.
- Dropout layers to prevent overfitting.
- Batch normalization and global max-pooling.
- Dense layer with a sigmoid activation function.
- Input size: sequences of word embeddings with a fixed length of 18 and dimensionality of 300.
Performance:

- Accuracy: 74%
- Precision:
   Negative: 75%
  
   Positive: 73%
- Recall:
   Negative: 71%
  
   Positive: 77%

**3. VGG-16 Model:**
Architecture:

Based on the popular VGG-16 architecture.
Performance:

- Accuracy: 75%
- Precision:
   Negative: 77%
  
   Positive: 73%
- Recall:
   Negative: 70%
  
   Positive: 79%
### Model Comparison
Each model captures n-gram features differently, and their performances indicate varying strengths in accuracy, precision, and recall metrics. The VGG-16 model, although more complex, achieved the highest recall, indicating better sensitivity to correctly identifying positive tweets.

## confusion matrix

## Results
**First CNN Model:** Balanced performance across accuracy and precision.

**Second CNN Model:** Better accuracy and recall performance.

**VGG-16 Model:** Highest recall, making it more suitable for tasks where identifying positive instances is crucial.
## Conclusion
This project demonstrates how different CNN architectures and a pre-trained word embedding model can be effectively used for sentiment analysis of tweets. The results highlight the strengths of each approach, providing insights into which model is best suited depending on the application context.


