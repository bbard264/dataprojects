# Dataset & Target

The dataset for this challenge is fictional and includes sales data for three items at two stores in three different countries. The target of the challenge is to predict a full year's worth of sales for these items. The dataset includes effects such as weekend and holiday effect, seasonality, etc. It is small enough to allow for the use of multiple modeling approaches. <br/>

## Files
train.csv - the training set, which includes the sales data for each date-country-store-item combination. <br/>
test.csv - the test set; your task is to predict the corresponding item sales for each date-country-store-item combination. Note the Public leaderboard is scored on the first quarter of the test year, and the Private on the remaining. <br/>
sample_submission.csv - a sample submission file in the correct format <br/>

https://www.kaggle.com/competitions/tabular-playground-series-jan-2022/data

# Exploring Data
the Data look like this
![image](https://user-images.githubusercontent.com/118603598/214538525-5623a2bd-039e-4052-872e-65d35bb23366.png)
- it's showing daily amount of sold in each product in different store and country
- 3 countrys are Finland, Norway and Sweden
- 2 stores are KaggleMart and KaggleRama
- 3 products are Kaggle Mug, Hat and Sticker
- since first day of 2015 till end of last day of 2018
- we have to preditct the amount of sold would happen in 2019 

![image](https://user-images.githubusercontent.com/118603598/214538428-112941cb-c3af-4dfb-b65c-e9a56d81f16e.png)
total sales each day in plot graph
- there is a trend
- there is a seasonality
- there is some outliner
