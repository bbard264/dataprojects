# Video Games Recommendation
here are file: https://drive.google.com/drive/u/0/folders/1n7IZZYySB78F9yDr3LFTALxti6vtjaCN <br/>
This project is about Recommendation using cosine/jac-card similarity that based on Critic review, user review and video game type. <br/>
following this step<br/>

## 1. scarp the Data form metacritic.com, the website that include comment and score from video game critic for each video game. the I have 3 csv file for analytics<br/>
- gamesdata.csv that contains infomation of video games<br/>
![image](https://user-images.githubusercontent.com/118603598/211808425-e0557625-b186-4cc7-8348-2bcbc82b31cb.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211808535-53e2761b-0360-4699-8139-8d1d6aa6793d.png)<br/>

- crireview.csv that contains review and score from critic<br/>
![image](https://user-images.githubusercontent.com/118603598/211808638-0a8028e1-9ad0-42e2-9d92-cb447628a125.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211809332-1f3d70d0-a047-403c-a93f-e62215365401.png)<br/>

- userreview.csv that contains review and score from user<br/>
![image](https://user-images.githubusercontent.com/118603598/211808732-748d257c-6eab-4fb8-840c-9e51ea2bba1c.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211809424-248eafac-cae4-420d-a9b4-40eeb563f093.png)<br/>

## 2. clearning data and prepare for analytics. In this process, I use pandas for operate the dataframe then I have a dataframe for calculate cosine similarity<br/>
![image](https://user-images.githubusercontent.com/118603598/211809659-7d2902e3-7699-47a5-9072-f741305dd1db.png)<br/>
![image](https://user-images.githubusercontent.com/118603598/211810020-38ff187d-c449-43b9-a3be-3e833bc22080.png)<br/>


## 3. calculated cosine similarity/Jac-card similarity for recommendationv
- get the genre information for gamesdata.csv to calculated jac-card similarity based on genre, this is a product-base recommendation (If the game have genre in common,these game should similarity each other)v

- get the critic score and user score for each video game to calculated cosine similarity based on score, this is a user-base recommendation (that I use infomation form review instead of purchasing, the ideas is if critic like some video game, they will give high score to the video game so if we like the game that this critic give hight score, we should like other video game that the critic give high score too.)<br/>

## 4. input the game ID, it will show the video games that have high cosine/jaccard similarity that means the high of cosine/jaccard similarity, the high similarity to the input game. then if you are customer and you like the input game much,you can use this output as infomation to find other video games that similar.<br/>
![image](https://user-images.githubusercontent.com/118603598/211811203-07d2de72-e66b-4530-94bc-c87b1c0abe5a.png)v



