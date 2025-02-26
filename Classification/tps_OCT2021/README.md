## Dataset & Target

For this competition, I will be predicting a binary target based on a number of feature columns given in the data. The columns are a mix of scaled continuous features and binary features. The data is synthetically generated by a GAN that was trained on real-world molecular response data.

Files
train.csv - the training data with the target column<br/>
test.csv - the test set; you will be predicting the target for each row in this file (the probability of the binary target)<br/>
sample_submission.csv - a sample submission file in the correct format<br/>

https://www.kaggle.com/competitions/tabular-playground-series-oct-2021/data

## Exploring Data
![image](https://user-images.githubusercontent.com/118603598/211374899-cd4632af-69b9-46bb-b8d5-2382cfb61af8.png) <br/>
* There are 1 million records in the dataset
* There are 285 features, with 45 binary features and 240 continuous features
* The 'target' is binary
* There are no missing values in the dataset.

## Analysis & Validation
* Using logistic regression to analyze this dataset because it can provide binary output, handle both binary and continuous features, and is suitable for handling a large number of features.<br/>

 ![image](https://user-images.githubusercontent.com/118603598/211375127-4f461514-e17f-4d1b-900b-4bbbf48679bf.png)<br/>


## Summarization
* the dataset have oth binary and continuous features and have 1 million records that I use logistic regression to predict a test data to create submission file<br/>
![image](https://user-images.githubusercontent.com/118603598/211375551-39e95e83-01bb-44ad-a424-bda41cfda512.png)
