# Movie Recommendation System: Project using R and Machine Learning

## Aim of the Project
The primary goal of this machine learning project is to build a recommendation engine that suggests movies to users. The project uses R to implement an Item-Based Collaborative Filtering algorithm, which helps recommend movies based on user preferences. This project enhances my skills in R programming, data science, and machine learning by applying them to a real-life dataset.

## Dataset Used
The MovieLens dataset was utilized for this project. It consists of:
- **ratings.csv**: Contains 105,339 ratings.
- **movies.csv**: Includes 10,329 movies.

## Essential Libraries
The following R libraries were used:
- `recommenderlab`
- `ggplot2`
- `data.table`
- `reshape2`

## Data Preprocessing
1. **Retrieving Data**: Data was loaded from the `movies.csv` and `ratings.csv` datasets.
2. **Data Conversion**: 
   - Converted `userId` and `movieId` columns into integers.
   - Created a one-hot encoding matrix for genres to make the data more usable.
3. **Sparse Matrix**: A sparse matrix (`realRatingMatrix` class) was created to represent the data in a format suitable for recommendation algorithms.

## Collaborative Filtering
Collaborative filtering suggests movies to users based on the preferences of other similar users. By computing similarities using operators like **cosine**, **pearson**, and **jaccard**, this method identifies users with similar movie preferences and recommends movies accordingly.

## Visualization
1. **User and Movie Similarity**: Visualized the similarity between users and movies using various similarity measures.
2. **Most Viewed Movies**: Displayed a bar plot showing the top most viewed movies. 'Pulp Fiction' emerged as the most watched, followed by 'Forrest Gump'.
3. **Heatmap of Movie Ratings**: A heatmap was created for the first 25 rows and columns of the ratings dataset to visualize user preferences.

## Data Preparation
The data was prepared in the following steps:
1. **Selecting Useful Data**: Focused on the top users and movies.
2. **Normalizing Data**: Adjusted ratings to remove bias (by normalizing to a common scale).
3. **Binarizing Data**: Transformed the ratings into binary values (1 for ratings above 3, and 0 otherwise) to simplify recommendations.

## Collaborative Filtering System
### Item-Based Collaborative Filtering
An item-based collaborative filtering approach was used, where similarities between movies were calculated based on ratings. This method suggests similar items to users who have rated them positively.

**Similarity Calculation**:  
For each movie \(i_1\) and another movie \(i_2\) rated by the same user, the similarity between them was computed.

### Model Training
- **Training Set**: The dataset was split into 80% training data and 20% testing data.
- **Parameter Exploration**: The default parameters were used for the Item-Based Collaborative Filtering. The value of \(k = 30\) was chosen, which means the top 30 most similar items were selected for recommendation.

## Building the Recommendation System
The recommender system was built using the following approach:
1. **Get Model**: Retrieved the recommendation model using the `getModel()` function.
2. **Similarity Visualization**: A heatmap was created to visualize the top 20 items based on similarity.
3. **Prediction**: The `predict()` function was used to generate movie recommendations for each user based on the trained model. A total of 10 movie recommendations were provided to each user.

## Conclusion
The project successfully built a recommendation system that provides personalized movie suggestions based on collaborative filtering, and visualized data trends to enhance the understanding of user behavior. 
