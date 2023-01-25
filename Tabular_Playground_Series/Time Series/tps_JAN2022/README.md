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
  
-The dataset includes daily sales data for three products, Kaggle Mug, Hat, and Sticker, at two stores, KaggleMart and KaggleRama, in three countries, Finland, Norway and Sweden. The data spans from the first day of 2015 until the end of 2018, and the task is to predict the sales for the year 2019.  
  
![image](https://user-images.githubusercontent.com/118603598/214538428-112941cb-c3af-4dfb-b65c-e9a56d81f16e.png)  
  
- There is a trend and seasonality in the sales.
- Some outliers are present in the data. 
  
![image](https://user-images.githubusercontent.com/118603598/214543032-ac3a214e-b0fa-4de2-bf4f-d5d35340b89e.png)  
  
- There are different seasonality patterns for each product.
  
![image](https://user-images.githubusercontent.com/118603598/214545579-f4c6d51a-62f6-4f28-bce3-9c876a07347a.png)  

![image](https://user-images.githubusercontent.com/118603598/214545619-5b5735d3-6712-4d42-89d9-0248263556ef.png)  

- No significant differences were found among the countries and stores, with correlation for stores > .99 and correlation for country > .95  
  
![image](https://user-images.githubusercontent.com/118603598/214651560-fe5fb4af-b5ce-414c-8567-f23999e9bcb6.png)  
  
- Upon zooming in on the distribution of the product Mug, a weekend effect was found.
  
![image](https://user-images.githubusercontent.com/118603598/214653145-48ff1f24-a09c-4801-b76f-8869d5e48a78.png)  
  
- There are holiday effects at the end of the year and at 3rd-4th months.
  
![image](https://user-images.githubusercontent.com/118603598/214654186-ebeba98a-4179-44c6-bd0d-9943642682ca.png)  
  
- Upon zooming in on sales each day in 3rd-4th months, there is an effect of Easter day that affects the day and week after Easter day.
  
![image](https://user-images.githubusercontent.com/118603598/214654652-f98886bc-e8d7-49d9-8f29-94635ce78565.png)
  
- Upon zooming in on sales each day in the last month of each year, there is an effect of Christmas day that affects the day after December 25th.  
- These effects were found in every product.

# Feature Engineer
- Separate analysis was conducted for each product, each store, and each country.  

![image](https://user-images.githubusercontent.com/118603598/214656063-1ef21f5b-c407-4586-ad8c-e7b6a3e59199.png)
  
- Features were added to each product based on the findings from the exploration.  
  
![image](https://user-images.githubusercontent.com/118603598/214656200-f285df0f-465e-4534-a816-03f4b45b6f58.png)
  

# Analysis & Validation
- XGBoost Regressor was used for forecasting sales of 2019.
  
- Modeling was performed for each product and validation was conducted.
  
![image](https://user-images.githubusercontent.com/118603598/214658169-54235704-a0e3-4e23-bff8-069472a54776.png)
  
- A file was created from the results, to submission at Kaggle.  
  
![image](https://user-images.githubusercontent.com/118603598/214658315-d2482e03-4ee8-40fd-94c6-ef8089ffa5cd.png)  
  
- The score from Kaggle is here.  
  
![image](https://user-images.githubusercontent.com/118603598/214658424-1a919948-2310-4e82-99e8-7954487dab75.png)






