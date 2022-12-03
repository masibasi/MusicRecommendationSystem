# MusicRecommendationSystem

### We built a recommendation program for “music”. The user enters in two songs and the main class ‘Music_Recommender’ recommends a list of songs relative to the entered two songs.
### Class ‘Music_Recommender’ calls other three classes that handles the following three filtering models : 
-	Collaborative Filtering – KNN Classifier
-	Content Based Filtering – Lyric based Cosine Similarity
-	Content Based Filtering – Music Features based Sigmoid calculation
### Program is also capable of retrieving new dataset from server by ‘Crawl_melon(self):’ function.

## Music_Recommender
> ' A Top-Level Class Music_Recommender is an all-in-one model music recommender Class. You can call different Models to get music suggested, used models: '
-	Collaborative Filtering – KNN Classifier
-	Content Based Filtering – Lyric based Cosine Similarity
-	Content Based Filtering – Music Features based Sigmoid calculation

> ### init 	( self, df_KNN_count, df_KNN_meta, df_Lyric, df_Feature):
> Initializing Function.
> Enter datasets provided for each filtering method.
> Preprocesses The Dataframe inside this function.

> ### KNN_Recommend(self, song1, song2):
> Function that calls Collaborative Filtering Model.
> Returns a list containing the recommended songs

### CB_Lyric_Recommend(self, song1, song2):
> Function that calls Content Based Filtering – Lyric based Cosine Similarity
> Returns a list containing the recommended songs

### CB_Feature_Recommend(self, song1, song2):
> Function that calls Content Based Filtering – Content Based Filtering – Music Features based Sigmoid calculation
> Returns a list containing the recommended songs

### Crawl_melon(self):
> Function that execute crawling on the website : “www.melon.com”
> Saves the dataframe to "melon_top100.csv"
 
## Collaborate_Recommender:
> Collaborate_Recommender is a class that handles KNN and Content based Filtering.

> ### init 	(self, metric, algorithm, k, data, decode_id_song):
> Initializing Function.
> Enter datasets provided for each filtering method.

> ### make_recommendation(self, new_song1, new_song2, n_recommendations):
> Creates recommendation for two songs.
> Returns a list containing the recommended songs

> ### _map_indeces_to_song_title(self, recommendation_ids):
> Internal function that gets reverse mapper

> ### _fuzzy_matching(self, song):
> Initiates Fuzzy Matching
 
## CB_Lyric_Recommender:
> CB_Lyric_Recommender is a class that handles Content based filtering that uses lyric data.

> ### init 	(self, metric, algorithm, k, data, decode_id_song):
> Initializing Function.
> Enter datasets provided for each filtering method.

> ### _print_message(self, song, recom_song):
> Prints out the result of the recommendation

> ### recommend(self, recommendation):
> Function that gets recommendation from 1 song
> Returns a list containing the recommended songs

> ### recommend2(self, recommendation):
> Function that gets recommendation from 2 song
> Returns a list containing the recommended songs


Reference : 
Dataset : https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset
http://millionsongdataset.com/

Data Crawling : https://dada-devdiary.tistory.com/34?category=994161

Content-based-filtering : https://towardsdatascience.com/the-abc-of-building-a-music-recommender-system-part-i-230e99da9cad

Collaborative-filtering : https://github.com/ugis22/music_recommender

