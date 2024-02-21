![SPAM](https://github.com/Mateusz-Szewczyk/spam-classification/assets/67056100/fc0ecb07-8a0e-4451-a490-cb11d8d3f3c3)

# Spam Classification Project

This project focuses on building a machine learning model for spam classification using Python. The goal is to predict whether a given message is spam or not.

## Overview
The project consists of several key components:

### Data Preparation:

- Loading a list of words from a CSV file named "words_list.csv" into a pandas Series.
- Loading comments data from a CSV file named "comments.csv" into a pandas DataFrame.
- Loading preprocessed comments data from a CSV file named "comments_data.csv" into a pandas DataFrame called comments_processed.

### Feature Extraction:

- Defining utility functions like message_to_words() and make_rows() to preprocess the text data and generate feature representations for each comment.

### Model Training and Evaluation:

- Splitting the data into training and testing sets.
- Defining several machine learning models like Logistic Regression, K-Nearest Neighbors, Random Forest, Support Vector Classifier (SVC), and LinearSVC.
- Training these models on the training data and evaluating their performance on the testing data.

### Hyperparameter Tuning:

- Performing hyperparameter tuning using RandomizedSearchCV for the Support Vector Classifier (SVC) model to find the best hyperparameters.

### Model Serialization:

- Saving the trained model to a pickle file named "final_model_test.pkl" using pickle.dump().

### Inference:

- Defining a function is_spam() that takes a message or list of messages as input and predicts whether each message is spam or not using the trained model.
- Testing the is_spam() function with some example messages.

## Usage
To use the spam classification functionality:

- Ensure you have the required dependencies installed (NumPy, pandas, scikit-learn).
- Clone the repository and navigate to the project directory.
- Run the Python script to preprocess the data, train the model, and perform inference.

## Example
Here's how you can use the is_spam() function to classify messages as spam or not:
```python
results = is_spam([
    "Beautiful photo! 😍",
    "Check out my profile for amazing deals!",
    "Get free followers now! Click the link in bio!",
    "Want to make $1000 a day from home? Click the link in my bio NOW!",
])
print(results)
```

#### Note
This README provides an overview of the spam classification project, its components, and how to use it. For detailed implementation and code explanations, refer to the project's source files.
