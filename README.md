# Get started:

- Download notebook file(.ipynb file) along with all the csv files.
- Upload it on Google colab and just run it 😊.
- That's it, GET YOUR RECOMMENDATION.

# Dataset - [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset):

For this implementation, I have used a subset of MovieLens dataset which is a combination of movies small dataset and The Movies Dataset.

This dataset includes the following items.

1. credits.csv
2. keywords.csv
3. links\_small.csv
4. movies\_metadata.csv
5. ratings\_small.csv

These files contain metadata for all 45,000 movies listed in Full Movielens Dataset. It consists of movies released on or before July 2017. Data points include cast, crew, plot keywords, budget, revenue, posters, release dates, languages, production companies, countries, TMDB vote counts, and vote averages. This dataset also has files containing 26 million ratings from 270,000 users for all 45,000 movies. Ratings are on a scale of 1-5 and have been obtained from the official GroupLens website.

# The approach used for the recommender system:

There are multiple approaches to develop a recommender system on a dataset like this. Some of the approaches are listed below.

- Simple Recommender
- Content-Based Recommender
- Item Based Recommender
- User-Based Recommender
- Metadata Based Recommender

Different approached uses different logic and data portions. For example, a simple recommender can use ratings and vote counts given in the dataset for movies to get the nearest neighbors.

For this programming assignment, I did Metadata Based approach combined with Item Based approach. Hence, I used the movies\_metadat.csv file to get the metadata for movies and credits.csv to get the cast and crew information to get more accurate results. I also used links\_small.csv to scale down my dataset further to work on limited resources. I also tried to use keywords from keywords.csv but there was a very minor difference in the result so went only with metadata and cast, crew data. Keep in mind that implementing the keywords approach was the same as implementing the credits approach.

# Dataset limit:

I scaled down my dataset using links\_small.csv which helped me a lot to develop the recommender system in time. After scaling down my dataset included 9,000 rated by 600 users with at least 100,0000 ratings and 3,600 tag applications which is a very decent amount of data to develop such a system.

After completing all the logic and steps, I tried to run the program again without scaling it down which took enormous time to run due to limited resources. If you choose to give up to 2 or 3 recommendation (k value) for any movie given as input, then my recommender system can take the entire dataset I mentioned above but with the expense of time and performance. Just for comparison, it nearly took two and a half hours with the number of recommendations set to 7.

# Time Complexity:

Due to the approach and the size of the dataset I have used I gained really good performance but maybe at the expense of time. I have used metadata, also, cast popularity feature to find similarity between movies which increased the performance but also increased the time taken by the algorithm.

My algorithm takes around a minute to give 12-15 recommendations to the movie given as an input which is not very huge, but it is not the better one also. There is not much difference when I increase the number of recommendations which is a very good thing.

If I use less metadata to find similarity, then I can surely decrease the time taken by my system, but it will not as accurate as it is right now. Better resources can always help when you want both performance and time complexity to its best.

# Performance:

Because of using a metadata-based approach, I gained a really good performance. The main factor behind this is because of genres and cast, crew information that I used to calculate the similarity between two movies. Almost all the genres are the same for the recommended movies and movies are related to each other which is amazing. I did not use any metrics to calculate the performance, but you can see the image below to better understand the performance that I have achieved. (zoom in to better see the results)

![](RackMultipart20210131-4-l9suc2_html_6018c51ae8229a42.png)

# Different ways to scale up:

There are multiple ways to scale up a recommender system like this. Some of them are listed below.

- Better resources – You can always enhance your system performance and time complexity by increasing your processing power.
- Normalized data – Precisely normalized data with all metadata can also help reduce time complexity and as a result, you can use more data to feed.
- Model Scaling.
- Using item-based collaborative filtering.

# References for KNN and k-fold cross-validation:

[https://www.kaggle.com/yesvenkat/knn-recommendation-system](https://www.kaggle.com/yesvenkat/knn-recommendation-system)
