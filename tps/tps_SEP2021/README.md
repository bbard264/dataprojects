## Dataset & Target

For this data, I will predict whether a customer made a claim upon an insurance policy. The ground truth claim is binary valued, but a prediction may be any number from 0.0 to 1.0, representing the probability of a claim. The features in this dataset have been anonymized and may contain missing values.

Files
train.csv - the training data with the target claim column<br/>
test.csv - the test set; you will be predicting the claim for each row in this file<br/>
sample_submission.csv - a sample submission file in the correct format<br/>

https://www.kaggle.com/competitions/tabular-playground-series-sep-2021/data

## Exploring Data
- 118 continous features
![image](https://user-images.githubusercontent.com/118603598/211275144-e800da0e-ee20-4eec-9f44-f4a21cbbee78.png)

- The target output 'claim' has binary outcomes of 0 and 1
![image](https://user-images.githubusercontent.com/118603598/211275188-423dc302-e2ec-45cb-8fae-cf34b4306c5c.png)

- Every feature has missing values, about 1.6% on average.
![image](https://user-images.githubusercontent.com/118603598/211283872-f1f38962-13e6-438e-be80-28dda728d935.png)

## Analysis &  Validation
- The XGBoost model will be used to handle missing values.

![image](https://user-images.githubusercontent.com/118603598/211274946-be8b66e8-d5d6-4a5c-b837-9bbe02f1b7ee.png)
## Exploring Result
![image](https://user-images.githubusercontent.com/118603598/211275112-97a102b6-cce6-494b-b09d-91c9a4ec8817.png)

## Summarization
Nothing more just use The XGBoost for classification to 0 or 1
and have AUC score = .73753 from Kaggle calculations

(An AUC score of 0.75 is generally considered to be a good performance for a classifier, but it can vary depending on the characteristics of your data and the specific goals of your project. If you have a relatively balanced dataset (i.e., the number of positive and negative examples are roughly equal) and you are aiming for high accuracy, then an AUC score of 0.75 might be acceptable. However, if you have an imbalanced dataset or you are focusing on a different evaluation metric (such as precision or recall), then an AUC score of 0.75 might not be sufficient.)
