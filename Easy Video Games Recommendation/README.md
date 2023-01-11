# Video Games Recommendation
here are file: https://drive.google.com/drive/u/0/folders/1n7IZZYySB78F9yDr3LFTALxti6vtjaCN <br/>
This project aims to create a recommendation system for video games using similarity metrics such as cosine and Jaccard similarity. Data was collected from the website metacritic.com, which includes reviews and scores from both critics and users. The collected data was then cleaned and prepared for analysis using the pandas library.. <br/>
The project consists of the following steps:<br/>

## 1. Create Dataset<br/>
Data was scraped from metacritic.com, resulting in three CSV files containing information about video games, critic reviews, and user reviews.<br/>
- gamesdata.csv that contains infomation of video games<br/>
![image](https://user-images.githubusercontent.com/118603598/211808425-e0557625-b186-4cc7-8348-2bcbc82b31cb.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211808535-53e2761b-0360-4699-8139-8d1d6aa6793d.png)<br/>

- crireview.csv that contains review and score from critic<br/>
![image](https://user-images.githubusercontent.com/118603598/211808638-0a8028e1-9ad0-42e2-9d92-cb447628a125.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211809332-1f3d70d0-a047-403c-a93f-e62215365401.png)<br/>

- userreview.csv that contains review and score from user<br/>
![image](https://user-images.githubusercontent.com/118603598/211808732-748d257c-6eab-4fb8-840c-9e51ea2bba1c.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211809424-248eafac-cae4-420d-a9b4-40eeb563f093.png)<br/>

## 2. clearning data <br/>
Data was cleaned and prepared for analysis using the pandas library, resulting in a dataframe for calculating cosine similarity.<br/>
![image](https://user-images.githubusercontent.com/118603598/211809659-7d2902e3-7699-47a5-9072-f741305dd1db.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211810020-38ff187d-c449-43b9-a3be-3e833bc22080.png)<br/>


## 3. Calculated cosine similarity/Jac-card similarity for recommendation.
In order to implement a recommendation system, we will calculate the Jaccard similarity and cosine similarity based on the genre and scores of the video games <br/>

- we will extract the genre information for each game in the dataset and use Jaccard similarity to determine the similarity between the games based on their common genres. This will serve as a product-based recommendation, as games with similar genres will be considered similar to each other<br/>

- we will extract the critic score and user score for each video game in the dataset. Using cosine similarity, we will then determine the similarity between the games based on these scores. This will serve as a user-based recommendation, as we will use information from reviews to determine which games are similar to each other. The idea behind this approach is that if a critic likes a certain video game and gives it a high score, it is likely that other games that receive high scores from the same critic will also be liked by users who enjoyed the first game.<br/>

## 4. Result , <br/>
The user inputs a game ID, and the system returns a list of games that have high cosine/Jaccard similarity to the input game. This serves as a guide for the user to find similar games they may enjoy.<br/>
![image](https://user-images.githubusercontent.com/118603598/211811203-07d2de72-e66b-4530-94bc-c87b1c0abe5a.png)



