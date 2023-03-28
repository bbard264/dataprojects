# Voice of Customers
This chapther we will explore and find out what customers say. We have a data that collect customer reviews of restaurant from Wongnai. And we will try to cluster customer reviews and looking for something new insight.
## Data Preparetion and Setup
we use KMeans for Clustering and "Wongnai Reviews - Small.csv" is our dataset\
![image](https://user-images.githubusercontent.com/95345008/147810695-ebcf0ae8-adee-410f-b01e-1f4ce4f2aeb4.png)\
## Document embedding and dimension reduction
Our data is texts, so we need to embed it to number that we can calculated by using Universal Sentence Encoder (USE)and reduce array dimensions using umap.
## Document Clustering using 
First, running kmeans with various number of k. evaluate no. of k based on the elbow plot\
![image](https://user-images.githubusercontent.com/95345008/147811009-705d5872-a136-409e-9e1b-ace2b6c589d8.png)\
From elbow plot, we find out that no. of clusters that fit the most then cluster into 3 clusters. after that, we merge all reviews of each cluster into one bit semtence.\
![image](https://user-images.githubusercontent.com/95345008/147811172-82b9b47c-3bce-4b3e-87ea-5122a7f2f500.png)
## Defined Clustering
After we clustering the reviews of customers, we need to explain what are each clusters and what each clusters mean. Then, we do more the result to easily explain it and find out characteristic of each clusters.\
 - removed a character that we don't want ([!@#$%^&*'])
 - removed any emoji
 - removed digit
 - removed white space
 - and removed stop words or word that is common or no meanning\
 ![image](https://user-images.githubusercontent.com/95345008/147811796-251d37d3-7cc7-492b-9325-a6a9d57c6858.png)
## Result Discusstion
After we try to cluster into 4 clusters(k=4), we find out that we can't define what those clusters mean. We reduce no. of clusters to 3 clusters then it looks more reliable. so we use 3 clusters instead of 4 clusters. and we can explain it here.\
- 1st cluster is peoples who love to go restaurant and normally review it on wongnai
- 2nd cluster is peolpes who love to go cafe and really like coffee
- 3rd cluster is peoples who love to go drink cafe (not like coffee) and they like bubble milk tea more than usual.
