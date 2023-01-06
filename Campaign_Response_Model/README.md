# Campaign Response Model
Campaign Response Model is the model that try to classify the customers who will respond to the new campaign based on data that collected from customers.<br />
## Let Explore!
Let see about our data this time! Here "Retail_Data_Response.csv" and "Retail_Data_Transactions.csv"! This data is about infomation about each customers that collected. Then, we want to predict that how probability of any customers will response to next marketing campaign by the dataset.<br />
## Prepare data
so we got these data "Retail_Data_Response.csv" and "Retail_Data_Transactions.csv" that we know Recency, Frequency, Monetary Value and CLV value from calculated "Retail_Data_Transactions.csv".<br />
<br />
![image](https://user-images.githubusercontent.com/95345008/147786850-bd42aa11-7035-43df-b3ac-824f9f0128da.png)<br />
<br />
And we know how they response to last campaign from "Retail_Data_Response.csv".<br />
<br />
![image](https://user-images.githubusercontent.com/95345008/147786874-510e1879-c404-4bf3-a01a-b46538c9407d.png)<br />
<br />
Then we merge 2 table into one.<br />
<br />
![image](https://user-images.githubusercontent.com/95345008/147786894-8e861b96-43b7-44e7-a65c-2753da0af196.png)<br />
<br />
## Creating train and test dataset
we split data into dataset,train dataset and test dataset<br />
<br />
![image](https://user-images.githubusercontent.com/95345008/147786925-8efec96e-3e3b-4db0-8713-199ad09f16fe.png)<br />
<br />
and we found that our data is unbalanced.<br />
<br />
![image](https://user-images.githubusercontent.com/95345008/147786938-68b08c07-b719-4973-bfb6-dff7546546ff.png)<br />
<br />
Then we need to fix it by SMOTE.<br />
<br />
![image](https://user-images.githubusercontent.com/95345008/147786949-6d768fde-e98a-45b4-88e3-ced6f8ab43ef.png)<br />
<br />
## Classification
### Logistic Regression
![image](https://user-images.githubusercontent.com/95345008/147820969-8bf8068d-02a7-47b2-8035-5064781effc5.png)

### Logistic Regression XGBoost
![image](https://user-images.githubusercontent.com/95345008/147820977-87ef254e-f2a1-4e1f-b748-c315752b1957.png)

### Random Forests
![image](https://user-images.githubusercontent.com/95345008/147820988-d8aeb3a3-78df-45ed-a9d9-11142e52fd48.png)

### Support Vector Machine
![image](https://user-images.githubusercontent.com/95345008/147820999-d661429e-2ad2-43ee-b4b8-89c0464424e6.png)

## Conclusion
After we classify our train and test dataset though those models, the best model is Logistic Regression with XGBoost. AUC Score frome Logistic Regression is quite high and is around AUC score of test dataset. AUC score of train dataset from Random Forests model is 1.0 but AUC score of test data set is belower than then it means this model overfit. SVM and KNN have less AUC score than Logistic Regression.
