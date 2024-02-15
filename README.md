# Recommendation System - My Anime List

This project focuses on building recommendation system for anime dataset. The Anime Dataset is a collection of data related to various anime titles, including information about the titles, genres, ratings, and more. This README file provides an overview of the dataset's contents and structure to help users understand and utilize the data effectively.

## Datset

This dataset contains:

- anime information for 13,379 animes
- user information for 1,123,284 myanimelist users
- 214,271 interactions between anime pairs (recommended and related animes)
- 5,048,994 interactions between user pairs (friendship)
- 223,812,614 interactions between users and animes

## Data Fields

1. **anime_id**: The unique identifier of the anime.
2. **anime_url**: The URL of the anime on MyAnimeList.
3. **title**: The name of the anime.
4. **synopsis**: A short description of the plot of the anime.
5. **main_pic**: The URL to the cover picture of the anime.
6. **type**: The type of the anime (e.g., TV, Movie, OVA).
7. **source_type**: The type of the source material for the anime (e.g., Manga, Light Novel).
8. **num_episodes**: The number of episodes in the anime.
9. **status**: The current status of the anime (Finished airing, Currently airing, or Not yet aired).
10. **start_date**: The start date of the anime.
11. **end_date**: The end date of the anime.
12. **season**: The season the anime started airing on (e.g., Winter 2020).
13. **studios**: A list of studios that created the anime.
14. **genres**: A list of genres associated with the anime (e.g., Action, Shonen).
15. **score**: The average score of the anime on MyAnimeList.
16. **score_count**: The number of users that scored the anime.
17. **score_rank**: The rank of the anime based on its score on MyAnimeList.
18. **popularity_rank**: The rank of the anime based on its popularity on MyAnimeList.
19. **members_count**: The number of users that are members of the anime.
20. **favorites_count**: The number of users that have the anime as a favorite.
21. **watching_count**: The number of users currently watching the anime.
22. **completed_count**: The number of users that have completed the anime.
23. **on_hold_count**: The number of users that have the anime on hold.
24. **dropped_count**: The number of users that have dropped the anime.
25. **plan_to_watch_count**: The number of users that plan to watch the anime.
26. **total_count**: The total number of users that have interacted with the anime (completed, plan to watch, watching, dropped, or on hold).
27. **score_10_count** to **score_01_count**: The number of users that scored the anime with a score from 1 to 10.
28. **clubs**: A list of MyAnimeList clubs the anime is part of.
29. **pics**: A list of URLs to pictures of the anime.

These data fields provide comprehensive information about various aspects of each anime title in the dataset, allowing for detailed analysis and exploration of anime-related trends and characteristics.

## Implemented Recommendation System

This project implements three types of recommendation systems:

- **Approach 1: Using TF-IDF** - This computes TF-IDF vectors for anime relevant features and calculates cosine similarity scores between anime titles. By inputting user's favorite anime IDs, it retrieves top recommendations based on similarities in synopses, offering personalized suggestions. It also handles user ID conversion and fetching anime titles from IDs for tailored recommendations

- **Approach 2: Genre based recommendation system** - This function generates genre-based anime recommendations for a user's favorite anime IDs. It identifies the genres of the user's favorites, then selects the top-ranked anime in each genre that is not already a favorite. The recommendations are presented with genre and anime name details.
  
- **Approach 3: Using Word2Vec** - Using this approach, it recommends similar anime titles to a given input anime title using Word2Vec vector representations and cosine similarity. It calculates the similarity scores between the input anime and all other anime, sorts them by similarity, and selects the top N similar anime titles.


- **Approach - 4: Using Glove** - This demonstrates how to convert preprocessed anime synopses into fixed-length vector representations using pre-trained GloVe word embeddings. Each word in the synopsis is represented by its GloVe word vector, and these vectors are averaged to create a single vector representation for the entire synopsis. The resulting vectors provide a numerical representation of the semantic content of each synopsis, which can be used for various natural language processing tasks.



## Technologies Used
The following technologies and libraries are used in this project:

- **Python**: The primary programming language for implementing the recommendation systems and data processing.
- **NumPy**: A fundamental library for numerical computing in Python, providing support for large, multi-dimensional arrays and matrices.
- **Pandas**: A powerful library for data manipulation and analysis, used for handling and preprocessing the dataset.
- **Scikit-learn**: A comprehensive machine learning library for Python, providing various tools for data preprocessing and similarity calculations.
- **Gensim**: A library for natural language processing, used for creating Word2Vec embeddings.
- **Matplotlib**: A plotting library for creating visualizations to analyze and present the results.
- **NLTK**: A Python library for NLP tasks like tokenization, stemming, lemmatization, parsing, and more, aiding text data processing.

  ## Made by - 

- Vishaka Nair [202318041]
- Srushti Bhagchandani [202318047]
- Shyam Saktawat [202311048]
- Ayush kumar Sahu [202311066]
- Abhishek Choudhary [202311067]

  ## Insights 

1. **Insights into User Preferences and Anime Popularity**
- Our analysis reveals significant insights into the relationship between anime score ranks and popularity, as well as the distribution of genres across the dataset. These findings have practical implications for content creators and platforms, suggesting that certain genres may be oversaturated or underserved. Additionally, the positive correlation between score ranks and popularity underscores the importance of quality in driving user engagement and satisfaction.
2. **Comparative Effectiveness of Recommendation Approaches**
- Our project provides valuable insights into the effectiveness of different recommendation approaches. For instance, while genre-based recommendations may be effective for new users, models using Word2Vec and GloVe embeddings offer a more personalized experience by understanding the nuanced preferences of individual users. This comparative analysis not only highlights the strengths and weaknesses of each approach but also guides future developments in recommendation systems.
3. **Implications for Future Work**
- The insights and methodologies developed in our project have broad implications for the future of recommendation systems. The novel use of Word2Vec and GloVe embeddings, in particular, suggests a promising direction for further research, potentially extending to other domains beyond anime. Additionally, the focus on diversity within recommendation lists opens up new avenues for improving user satisfaction and engagement across recommendation platforms.

## Conclusion
In conclusion, our project makes significant contributions to the field of recommendation systems through its innovative use of NLP techniques, comprehensive approach to system development, and insightful analysis of user data. By pushing the boundaries of how we understand and implement recommendations, our work not only enhances the user experience for anime viewers but also offers a blueprint for future advancements in personalized content discovery
  
  

