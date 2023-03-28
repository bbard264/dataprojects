# Customer Segmentation
Customer segmentation is the process by which you divide your customers up based on common characteristics
![image](https://user-images.githubusercontent.com/95345008/147415999-30f34133-e53a-4615-9c9b-1a3ec8e12405.png)

## Let Explore!!
before explore, we use Python and PyCaret Library for analytic and cluster this customer segmentation and the data that we use here are 'Supermaket Data'


### 1. Set up
- Load "[Supermarket Data.csv](https://drive.google.com/file/d/1CBuHPnAf1FbBJxiMxBJxvtnS4DMJrEdD/view?usp=sharing)" 
- Instrall PyCaret 
- Import necessary libraries (pandas,numpy)

### 2. Explore Data and find new features
Let see the Supermarket Data that we have a lot of infomation about customer form the supermarket.

Example data frame!
![image](https://user-images.githubusercontent.com/95345008/147416153-abf7df40-4040-4c34-9192-cca66c7a6e82.png)
 
After we explore the data, we prepare customer single view by calculating some of features that we have, here are them.

- Calculated 'Total visits' 
- Calculated 'Ticket size'
- Calculated 'Total no. of SKUs'

After that we try to find new features that we think it impact to our clustering. In fact, we should research that which features really impact to the clustering.
- added 'max_date'
- added 'total_days'
- added 'recency'

Here are lasted data!

![image](https://user-images.githubusercontent.com/95345008/147416215-9f078455-4a78-4abd-9c31-927f3f50c6f0.png)


### 3. Clustering!!
now the data is ready for clustering! let's go!
#### Compare model performance
after we let the data to all of these cluster model, we have to find out that which model is highest performance
so that we find out Spectral and KMeans Clustering is good to go for it\
![image](https://user-images.githubusercontent.com/95345008/147416293-9618939d-9c29-4bfb-ab6f-dc8bcc81b698.png)

#### Spectral Clustering 
here is the result of Spectral Clustering
![image](https://user-images.githubusercontent.com/95345008/147416300-e69e562c-c002-4a52-a7b4-1a53dd44434e.png)
(after see this graph so we think this model won't work)

#### KMeans Clustering
here is the result of KMeans Clustering
![image](https://user-images.githubusercontent.com/95345008/147416322-f6b141ad-8f03-4d27-a6d8-dee2c1c669c5.png)
more reliable so we think we can go fot it form KMeans Clustering

K= 4, Distortion Score Elbow for KMeans Clustering
that means we have to use K=4 in KMeans Clustering
![image](https://user-images.githubusercontent.com/95345008/147416360-3c195a9a-87f0-4b4c-bcd8-67b86656fe3b.png)
Silhouette plot say there have 4 centers of KMeans Clustering
![image](https://user-images.githubusercontent.com/95345008/147416364-d32e0142-e26a-4e58-920a-2201b6f56de9.png)

### 4. Interpret the results
Now, we have to interpret what that is mean? what is the clustering say?
for answering the questions, we have to find out characteristics of any clustered data that we need to explore more!
![image](https://user-images.githubusercontent.com/95345008/147416407-f450b26e-d733-4882-ba0d-65be79e85f9c.png)
![image](https://user-images.githubusercontent.com/95345008/147416410-878c9427-deb6-4813-acc6-580268f0631b.png)
![image](https://user-images.githubusercontent.com/95345008/147416414-ede12c69-4fae-4fdc-8225-260c167f8185.png)
![image](https://user-images.githubusercontent.com/95345008/147416416-3cd153cd-147d-46a7-91f4-860d3f285fc7.png)
![image](https://user-images.githubusercontent.com/95345008/147416421-1f1aa39f-1634-4295-a364-82292e655075.png)
![image](https://user-images.githubusercontent.com/95345008/147416422-e57287e4-ac43-4b95-8711-644f88bac8be.png)
![image](https://user-images.githubusercontent.com/95345008/147416432-65dd29c4-f619-48cd-b1a9-c4e3114fd1e6.png)
![image](https://user-images.githubusercontent.com/95345008/147416435-6e694785-e1ac-4dfd-9349-3e835f54a41a.png)
![image](https://user-images.githubusercontent.com/95345008/147416441-d0420498-62cd-4b43-9a16-dbfd2e9ae87f.png)

after that, we can interpret the results fo these clustering and can name all of the clustering :D

----------------------------------------------------------------------
[The cluster 0 : Not much in this customer group, highest ticket size but Recency is quite high. Potentially deal a long-term contract selling, delivery at their place and cross-selling for another potential products.]

[The cluster 1 : Rich customer, not much in quantity but high value and profitable, mainly non food purchasing, very active customers. Should be the customers near the shop location. They are our treasure, bind them with the premium membership with exclusive deal, offer and make sure they we can maintan them. Considerr to brach new line with the popular "non food" product]

[The cluster 2 : The most in quantity customers, low ticket size and high recency. Potential the normal customer, routinely check the price competitive of our products]

[The cluster 3 : 2nd Most customers, Active user, Purchasing ast small shop mainly, Not much total spent. Try to upselling with more premium products.]

----------------------------------------------------------------------

In fact, you have to find more any research or information that can support your conclusion to make more reliable and practical.
