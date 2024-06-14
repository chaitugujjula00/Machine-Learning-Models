# Movie Recommendation System

This project is a movie recommendation system that suggests movies based on the user's favorite movie. The recommendation is based on the similarity of movie plots using the TF-IDF (Term Frequency-Inverse Document Frequency) Vectorizer.

## Dataset

The dataset needed for this project can be downloaded from [https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbU9Za2xZak1sTkcyNzQ5LVBJaEw5UzNreF8zQXxBQ3Jtc0trSzhZZWRPdW41emRXeEdOelBHcnl0aVlWb0ZMbUhJMUI1Z0NvZjFXai03eHp0LVVROTllaGRKOUVFRE1IbGs1UGhySGx3NFBYRVFYWEY0NmxhNkUwYUQ2S3NfWlloc014UWdVckpyN2J0TklTUkU2dw&q=https%3A%2F%2Fdrive.google.com%2Ffile%2Fd%2F1cCkwiVv4mgfl20ntgY3n4yApcWqqZQe6%2Fview%3Fusp%3Dsharing&v=7rEagFH9tQg]. Ensure you have the dataset saved as `movies.csv` in the same directory as your script.

## Installation

To run this project, you need to have Python installed along with the following libraries:
- pandas
- numpy
- scikit-learn
- difflib

You can install these libraries using pip:

```bash
pip install pandas numpy scikit-learn
```

## Preprocessing

The preprocessing of the movie dataset involves creating a TF-IDF matrix of the movie plots. This matrix helps in calculating the cosine similarity between different movies.

### Steps:
1. **Load the dataset:** Read the movie dataset using pandas.
2. **Vectorize the plot:** Use the `TfidfVectorizer` from scikit-learn to convert the text data into numerical data.
3. **Calculate similarity:** Compute the cosine similarity between the TF-IDF vectors of the movie plots.

## Running the Recommendation System

The recommendation system works as follows:
1. **User Input:** The user is prompted to enter their favorite movie name.
2. **Find Close Matches:** The system searches for the closest matching movie titles from the dataset.
3. **Get Similarity Scores:** For the closest match, the system calculates the similarity scores with all other movies.
4. **Sort and Recommend:** The movies are sorted based on their similarity scores in descending order, and the top recommendations are displayed.

## Usage

1. Ensure you have the dataset `movies.csv` in the same directory as your script.
2. Run the script.
3. Enter your favorite movie name when prompted.
4. The script will output a list of recommended movies based on your input.

## Conclusion

This movie recommendation system uses TF-IDF vectorization to capture the similarity between movie plots. It provides personalized movie recommendations based on the plot content, making it a useful tool for discovering new movies similar to your favorites.