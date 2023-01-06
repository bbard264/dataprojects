# Product Recommendation
Product Recommendation is how we can recommend our other products that customers didn't buy it. We try to recommend customers based on what that customer purchased and others purchased seeing how they are similarity
## Let explore!
This time, we create questionnaire asking peoples that buy or not buy each product. The data we collected look like this.\
![image](https://user-images.githubusercontent.com/95345008/147813134-d7a31ea4-6e35-4cae-b6d7-33c8f18101e6.png)
## Prepared Data
After we got the dataframe, we clean it first by
- removing NaN
- removing product that is not reliable
- removing some observation that is not reasonable
## The Apriori algorithm
### What is Apriort algorithm
Apriori algorithm is a sequence of steps to be followed to find the most frequent itemset in the given database\
\
**Antecedent** (IF): This is an item/group of items that are typically found in the Itemsets or Datasets.\
**Consequent** (THEN): This comes along as an item with an Antecedent/group of Antecedents.\
**Lift**: Lift indicates the strength of a rule over the random occurrence of A and B. It basically tells us the strength of any rule.\
**Support**: It gives the fraction of transactions which contains item A and B. Basically Support tells us about the frequently bought items or the combination of items bought frequently\
**Confidence**: It tells us how often the items A and B occur together, given the number times A occurs.\
\
![image](https://user-images.githubusercontent.com/95345008/147813335-c53915b7-1d0d-42ae-9aaf-08df9d281440.png)\
\
This table show that how the Apriori algorithm do thing.
- we set 'lift' > 1
- we set 'confidence' > 0.7\
## Result Discussion
After we saw the result of product recommendation, we can recommend people who buy running shoes buy truly wireless earbuds and on the other hand too. we also recommend who buy online course buy Ebook or seat cushion and on the other hand too.
