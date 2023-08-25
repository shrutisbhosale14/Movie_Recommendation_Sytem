# Movie Recommendation Sytem
Recomendation System Project

• Project Name : Movie Recommendation System

-	Table of Content: 
1.	Reason to take this DataSet, 
2.	Workdone, 
3.	Conclusion, 
4.	Result

•	Reason to take this DataSet, 
Wondered how Google comes up with movies that are similar to the ones you like.
There are (mostly) three ways to build a recommendation engine:
1)	Popularity based recommendation engine
2)	Content based recommendation engine    
3)	Collaborative filtering based recommendation engine

We are going to implement a Content based recommendation system using the scikit-learn library.

-	Content based recommendation engine
This type of recommendation systems, takes in a movie that a user currently likes as input.
Then it analyzes the contents (storyline, genre, cast, director etc.) of the movie to find out other movies which have similar content.
Then it ranks similar movies according to their similarity scores and recommends the most relevant movies to the user.


•	Workdone :

-	First load the dataset – read the csv file 
-	Check the first 5 values by using head()
-	Then check the last 5 values using the tail()
-	Check the data shape and info by using shape() and info()
-	Then check if the dataset contains any duplicate values.
-	If we go through the dataset, we can see that the dataset contains many more extra info columns and we don't need all of them.
-	So, we choose keywords, cast, genres, director columns to use as features set which is the main content of movie.
-	Then check the first 20 titles of the movies.
-	Create a function for combining the values of these columns into a single string
-	Now, we need to call function over each row of our dataframe.
-	But, before doing that we need to clean and preprocess the data for our use.
-	We will fill all the NaN values with blank string in the dataframe.
-	Fill the null values with the blank strings

-	We have obtained the combined strings, we can now feed these strings to a CountVectorizer() object for getting the count matrix.

-	Now, we need to obtain the cosine similarity matrix from the count matrix.

cosine_sim = cosine_similarity(count_matrix)

-	Now, we will define two helper functions to get movie title from movie index and other.

-	The next step is to get the title of the movie that the user currently likes.

-	Then we will find the index of that movie. After that, we will access the row corresponding to this movie in the similarity matrix.

-	We will get the similarity scores of all other movies from the current movie. Then we will get all the similarity scores of that movie to make a tuple of movie index and similarity score.

-	We will sort the list similar_movies according to similarity scores in descending order.

-	Since the most similar movie to a given movie will be itself, we will discard the first element after sorting the movies

•	Conclusion, 

Now, we will run a loop to print first 5 entries from sorted_similar_movies list
-	Top 5 similar movies to Avatar are:

I.	Guardians of the Galaxy
II.	Aliens
III.	Star Wars: Clone Wars: Volume 1
IV.	Star Trek Into Darkness
V.	Star Trek Beyond

•	Result: 

The above are the recommended similar movies from user's like (interest)
Here we have used Movie named 'Avatar' as the user's interest. If we search on google for similar movies as 'Avatar' we can find above similar interest listed movies name.

# THANK YOU
