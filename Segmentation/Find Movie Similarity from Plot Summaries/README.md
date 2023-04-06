# Find Movie Similarity from Plot Summaries
Many movies are created based on various interesting themes. Some people like superhero movies, while others like horror movies. However, just knowing the name or genre of a movie may not be enough to determine if we like it or not. Therefore, we need to read the plot of these movies first to find out if we like them.

Moreover, with so many movies available nowadays, it can take a long time to read the plot of each movie to find the ones we like. In this notebook, we will quantify the similarity of movies based on their plot summaries available on IMDb and Wikipedia, and then cluster them into groups. This will allow us to find movies with similar plots to the ones we like. We'll create a dendrogram to represent how closely the movies are related to each other

Outline
1. Importing the dataset 
    - these dataset get from wikipedia and imdb that contain plot on each movies.
    - ![image](https://user-images.githubusercontent.com/118603598/230375810-15d3e66b-ae0c-4854-a304-b4132ed092e7.png)

2. Pre Proccessing Data
    1. Combine Wikipedia and IMDb plot summaries.
        - Combining plot summaries from both Wikipedia and IMDb will provide a larger dataset for analysis and more accurate results.
        - ![image](https://user-images.githubusercontent.com/118603598/230375883-fc2b5fd5-6f28-498e-ad8e-5e735d14532e.png)
    2. Tokenization
        - Tokenization breaks down the plot summaries into individual words for analysis.
        - "\n                        Today (May 19, 2016) is his only daughter's wedding.", 'Vito Corleone is the Godfather.'
        - to this -> ['Today', 'May', 'is', 'his', 'only', 'daughter', "'s", 'wedding']
    3. Stemming
        - Stemming reduces words to their root form for more effective analysis.
        - after stemming ['today', 'may', 'is', 'his', 'onli', 'daughter', "'s", 'wed']
    4. Combining Tokenize & Stem
        - Combining tokenization and stemming will create a more efficient dataset for analysis.
    5. Create TfidfVectorizer and Fit transform TfidfVectorizer
        - TfidfVectorizer will convert the plot summaries into numerical vectors for analysis.
        - Fit transform TfidfVectorizer to convert the plot summaries into numerical vectors for clustering.
        - ![image](https://user-images.githubusercontent.com/118603598/230376158-ef53fa0b-c595-4570-a132-61bc51f64bb8.png)

3. Modeling
    1. Import KMeans and create clusters
        - Importing KMeans and creating clusters will group the movies with similar plots together.
        - ![image](https://user-images.githubusercontent.com/118603598/230376293-55ec4a7d-7dfa-4237-a5f9-2753fbcbc645.png)
    2. Calculate similarity distance
        - Calculating similarity distance will help identify which movies are more similar to each other.
        - ![image](https://user-images.githubusercontent.com/118603598/230376354-58127a8e-555a-43e2-89ec-3ebbbeae9f5f.png)

4. Validation
    - Evaluating the performance of the clustering algorithm
    - ![image](https://user-images.githubusercontent.com/118603598/230376395-d32a0cac-1222-49fa-b0c9-24d60fef3eab.png)
    - ![image](https://user-images.githubusercontent.com/118603598/230376472-d5fba43a-b938-41ab-9639-e1d2c50714ed.png)
    - ![image](https://user-images.githubusercontent.com/118603598/230376568-ed061de3-ee24-4875-9347-791a625235bc.png)
    
5. Data Visuialization
    1. Import Matplotlib, Linkage, and Dendrograms
        - Importing Matplotlib, Linkage, and Dendrograms will create a visual representation of the relationship between the movies.
    2. Create merging and plot dendrogram
        - Creating merging and plotting dendrograms will allow for a better understanding of the clusters formed and which movies are more closely related to each other.
        - ![image](https://user-images.githubusercontent.com/118603598/230376642-d0ae9a68-caa7-48cb-8090-0ea92b3fae6c.png)

