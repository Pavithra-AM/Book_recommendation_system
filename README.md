# Book_recommendation_system
This project is a collaborative filtering-based recommendation system that predicts book ratings and recommends books to users based on their preferences and past interactions. Using the Surprise library, we employ matrix factorization with Singular Value Decomposition (SVD) to provide accurate recommendations.

Project Overview
The Book Recommendation System includes two main recommendation methods:

Popularity-Based Recommendations: Recommends the most popular books.
Collaborative Filtering Recommendations: Recommends personalized books for each user using collaborative filtering.
Features
Collaborative Filtering: Utilizes SVD to make personalized recommendations based on user-item interactions.
Popularity-Based Recommendations: Suggests books that are popular across all users.
TF-IDF for Content Similarity (if implemented): Helps to recommend books based on text features like book titles, authors, and publishers.
Evaluation Metrics: Uses RMSE (Root Mean Squared Error) to evaluate the accuracy of predictions.
Dataset
The dataset contains:

User ratings for different books
Metadata for books (e.g., title, author, publisher)
Make sure to structure the data as follows:

Books.csv: Contains ISBN, Book-Title, Book-Author, and Publisher.
Ratings.csv: Contains User-ID, ISBN, and Book-Rating.
Requirements
Python 3.x
pandas: Data manipulation
scikit-learn: TF-IDF vectorizer
surprise: Collaborative filtering and matrix factorization
numpy: Array manipulations
Install the dependencies with:

bash
Copy code
pip install pandas scikit-learn scikit-surprise numpy
Project Structure
plaintext
Copy code
├── Books.csv                  # Book details
├── Ratings.csv                # User ratings
├── book_prediction_system.py   # Main code file
└── README.md                  # Project documentation
Usage
1. Data Preparation
Make sure the data files (Books.csv, Ratings.csv) are in the same directory as the main Python script. Ensure that pandas loads them without issues, and clean any missing values.

2. Running the Model
Run the main Python file to execute the recommendation system.

bash
Copy code
python book_prediction_system.py
3. Popularity-Based Recommendations
The system outputs popular books based on the average ratings across all users. Adjust the threshold to filter popular books according to your preference.

4. Collaborative Filtering Recommendations
Use the function get_collaborative_recommendations(user_id, num_recommendations=5) to get personalized recommendations for any user.

Example:

python
Copy code
user_id = 12345  # Replace with an actual User-ID
print(get_collaborative_recommendations(user_id, num_recommendations=5))
This will output the top recommended books for the specified user.

Evaluation
The collaborative filtering model’s accuracy is measured using RMSE. After training, the model evaluates predictions on the test data, and RMSE is printed to help assess performance.

Example Output

Top 5 recommended books for User-ID 12345:

- Free (Estimated Rating: 9.75)
- The Blue Day Book: A Lesson in Cheering Yourself Up (Estimated Rating: 9.50)
- Frindle (Estimated Rating: 9.45)
- The Coldest Winter Ever (Estimated Rating: 9.30)
- The Greatest Discovery (Estimated Rating: 9.20)
