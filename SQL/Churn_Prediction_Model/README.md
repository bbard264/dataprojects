# Churn Prediction Model
Churn Prediction Model is part for Customer Movement Analysis that divide customers into 4 categories defined by this\
\
![image](https://user-images.githubusercontent.com/95345008/147817008-57024a0c-78e5-45cf-92da-5ba38e5414db.png)
\
Current: made purchases this month (M)\
Previous: made purchases last month (M-1)\
Before: made purchase before last month (< M-1)
## Let explore
This time we have data set 'Supermarket.csv' that have enough data to calculate the churn prediction but we need to preapare the data first.\
\
![image](https://user-images.githubusercontent.com/95345008/147817296-9054716d-f338-48b9-a890-3888ac467c88.png)
## SQL BigQuery
We use SQL BigQuery([here](https://github.com/ppond264/CRM-Analytics/blob/main/Churn_Prediction_Model/ChurnPredictionSQL.sql)) for prepare the report\
\
![image](https://user-images.githubusercontent.com/95345008/147817334-c19a32f5-fb1c-4c7c-b1e0-0271075953a6.png)

## Report
And then we use power bi to create this report\
\
![ChurnPrediction-dashboard](https://user-images.githubusercontent.com/95345008/147816520-375dc0e2-fc6c-4768-aa86-473e1223d429.jpg)
