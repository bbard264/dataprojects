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

![image](https://user-images.githubusercontent.com/118603598/214543032-ac3a214e-b0fa-4de2-bf4f-d5d35340b89e.png)  
- there are different seasonality in each product  
![image](https://user-images.githubusercontent.com/118603598/214545579-f4c6d51a-62f6-4f28-bce3-9c876a07347a.png)  
![image](https://user-images.githubusercontent.com/118603598/214545619-5b5735d3-6712-4d42-89d9-0248263556ef.png)  
- there are no different among countrys and store
- correlation for stores > .99
- correlation for country > .95

After I zoom in distribution of product mug varies week day, I found that there are weekend effects.  
![image](https://user-images.githubusercontent.com/118603598/214651560-fe5fb4af-b5ce-414c-8567-f23999e9bcb6.png)  
- weekday 0 - 4 are working day and weekday 5, 6 are weekend  
![image](https://user-images.githubusercontent.com/118603598/214653145-48ff1f24-a09c-4801-b76f-8869d5e48a78.png)  
- there are holiday effects at end of the year  
- there are holiday effects at 3 - 4 months  
![image](https://user-images.githubusercontent.com/118603598/214654186-ebeba98a-4179-44c6-bd0d-9943642682ca.png)  
- I zoom in sales each day in 3 - 4 months, there are a effect of easter day that affect that day and week after easter day.
![image](https://user-images.githubusercontent.com/118603598/214654652-f98886bc-e8d7-49d9-8f29-94635ce78565.png)
- I zoom in sales each day in the last month of each year, there are a effect of christmas day that affect the day after 25 DEC.
- I found these effect in every products

# Feature Engineer
- seperate analysis each product each store and each country. 
![image](https://user-images.githubusercontent.com/118603598/214656063-1ef21f5b-c407-4586-ad8c-e7b6a3e59199.png)
- In each product I add feature that create form what I exploring.  
![image](https://user-images.githubusercontent.com/118603598/214656200-f285df0f-465e-4534-a816-03f4b45b6f58.png)

# Analysis & Validation
- Using XGBoost Regressor for forecasting sales of 2019  
- modeling for each product and validation  
![image](https://user-images.githubusercontent.com/118603598/214658169-54235704-a0e3-4e23-bff8-069472a54776.png)
- create file form result  
![image](https://user-images.githubusercontent.com/118603598/214658315-d2482e03-4ee8-40fd-94c6-ef8089ffa5cd.png)  
- score form Kaggle is here
![image](https://user-images.githubusercontent.com/118603598/214658424-1a919948-2310-4e82-99e8-7954487dab75.png)






