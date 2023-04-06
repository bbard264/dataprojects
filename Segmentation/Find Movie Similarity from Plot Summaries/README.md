# Find Movie Similarity from Plot Summaries
Many movies are created based on various interesting themes. Some people like superhero movies, while others like horror movies. However, just knowing the name or genre of a movie may not be enough to determine if we like it or not. Therefore, we need to read the plot of these movies first to find out if we like them.

Moreover, with so many movies available nowadays, it can take a long time to read the plot of each movie to find the ones we like. In this notebook, we will quantify the similarity of movies based on their plot summaries available on IMDb and Wikipedia, and then cluster them into groups. This will allow us to find movies with similar plots to the ones we like. We'll create a dendrogram to represent how closely the movies are related to each other

Outline
1. Importing the dataset 
    - these dataset get from wikipedia and imdb that contain plot on each movies.

![image](https://user-images.githubusercontent.com/118603598/230375489-51b86faa-23be-4666-9acf-71505b8a91e4.png)


2. Pre Proccessing Data
    1. Combine Wikipedia and IMDb plot summaries.
        - Combining plot summaries from both Wikipedia and IMDb will provide a larger dataset for analysis and more accurate results.
    2. Tokenization
        - Tokenization breaks down the plot summaries into individual words for analysis.
    3. Stemming
        - Stemming reduces words to their root form for more effective analysis.
    4. Combining Tokenize & Stem
        - Combining tokenization and stemming will create a more efficient dataset for analysis.
    5. Create TfidfVectorizer and Fit transform TfidfVectorizer
        - TfidfVectorizer will convert the plot summaries into numerical vectors for analysis.
        - Fit transform TfidfVectorizer to convert the plot summaries into numerical vectors for clustering.

3. Modeling
    1. Import KMeans and create clusters
        - Importing KMeans and creating clusters will group the movies with similar plots together.
    2. Calculate similarity distance
        - Calculating similarity distance will help identify which movies are more similar to each other.

4. Validation
    1. Evaluating the performance of the clustering algorithm
    
5. Data Visuialization
    1. Import Matplotlib, Linkage, and Dendrograms
        - Importing Matplotlib, Linkage, and Dendrograms will create a visual representation of the relationship between the movies.
    2. Create merging and plot dendrogram
        - Creating merging and plotting dendrograms will allow for a better understanding of the clusters formed and which movies are more closely related to each other.
