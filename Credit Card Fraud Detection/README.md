# Credit Card Fraud Detection using Logistic Regression

This project is a machine learning application for detecting fraudulent credit card transactions using logistic regression. The dataset is highly imbalanced, containing significantly more normal transactions than fraudulent ones. The goal is to build a model that can accurately identify fraudulent transactions.

## Dataset

The dataset for this project can be downloaded from [https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbFhBSGhpenBlUFlKdno2VEw5UHlrRFhESmVkZ3xBQ3Jtc0tsWmxHai1POG5QbFNlbS1nSjZCWllWMTVuRkxjbVhpNjU2dHluRGtlckxIUkpzVnVmUXZCLTBkalJ2cmFzN3llZG5jLVFLa2VwNFo5M1U0S25VUzktb2lxeF90RWlWVGlpQ1EyMlBKZ3NXX3BNTEJoRQ&q=https%3A%2F%2Fwww.kaggle.com%2Fmlg-ulb%2Fcreditcardfraud&v=NCgjcHLFNDg]. Ensure you have the dataset saved as `creditcard.csv` in the same directory as your script.

## Installation

To run this project, you need to have Python installed along with the following libraries:
- numpy
- pandas
- scikit-learn

You can install these libraries using pip:

```bash
pip install numpy pandas scikit-learn
```

## Data Preprocessing

1. **Load the dataset:** Read the credit card dataset using pandas.
2. **Explore the dataset:** Display the first few rows and check the information and distribution of the classes.
3. **Check for missing values:** Ensure there are no missing values in the dataset.
4. **Separate legitimate and fraudulent transactions:** Divide the data into two separate DataFrames for normal and fraudulent transactions.
5. **Statistical analysis:** Perform a statistical analysis on the amount of money involved in both types of transactions.
6. **Under-sampling:** Create a balanced dataset by under-sampling the majority class (normal transactions) to match the number of fraudulent transactions.
7. **Concatenate the samples:** Combine the under-sampled normal transactions with the fraudulent transactions to form a new dataset.
8. **Split the data:** Divide the dataset into features (X) and target (Y), and then split it into training and testing sets.

## Model Training

1. **Logistic Regression:** Use logistic regression for model training.
2. **Train the model:** Train the logistic regression model using the training data.

## Model Evaluation

1. **Accuracy Score:** Evaluate the model using the accuracy score for both training and testing data.

## Steps to Run the Project

1. **Import Dependencies:**
   - numpy for numerical operations.
   - pandas for data manipulation.
   - train_test_split from scikit-learn for splitting the dataset.
   - LogisticRegression from scikit-learn for model training.
   - accuracy_score from scikit-learn for model evaluation.

2. **Load and Explore the Dataset:**
   - Load the dataset using `pd.read_csv('creditcard.csv')`.
   - Display the first 5 rows using `credit_card_data.head()`.
   - Check the dataset information using `credit_card_data.info()`.
   - Check for missing values using `credit_card_data.isnull().sum()`.
   - Display the distribution of classes using `credit_card_data['Class'].value_counts()`.

3. **Separate and Analyze Data:**
   - Separate legitimate and fraudulent transactions.
   - Perform statistical analysis on the transaction amounts.
   - Compare the mean values of both classes using `credit_card_data.groupby('Class').mean()`.

4. **Under-sampling:**
   - Create a balanced dataset by sampling legitimate transactions.
   - Combine the samples to form a new dataset.
   - Verify the new dataset using `new_dataset.groupby('Class').mean()`.

5. **Feature and Target Selection:**
   - Define features (X) by dropping the 'Class' column.
   - Define target (Y) as the 'Class' column.

6. **Split the Data:**
   - Split the data into training and testing sets using `train_test_split()`.

7. **Train the Model:**
   - Instantiate the logistic regression model.
   - Train the model using `model.fit(X_train, Y_train)`.

8. **Evaluate the Model:**
   - Predict on training data and calculate accuracy.
   - Predict on testing data and calculate accuracy.
   - Print the accuracy scores for both training and testing data.

## Conclusion

This credit card fraud detection system uses logistic regression to classify transactions as legitimate or fraudulent. The model is trained on a balanced dataset created by under-sampling the majority class and evaluated using accuracy scores.