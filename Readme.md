# Overview

# Overview

This is a beginner-level sentiment analysis project that classifies IMDB movie reviews as positive or negative. It uses TF-IDF to convert review text into numerical features and Logistic Regression for classification.
# Dataset

The dataset I have made use of in this project is IMDB dataset. The dataset has 50,000 entries and two columns.

**1) Review:** Acts as the feature that we train the model upon.

**2) Sentiment:** This is the target label that we will be predicting.

The dataset contains an equal number of positive and negative reviews 
- 25,000 positive reviews
- 25,000 negative reviews. 

The dataset does not contain any null values but it had 418 duplicates which were removed using df.drop_duplicates() function.


# Libraries

The Libraries I have made use of in this project are: Pandas and sklearn. Several components were imported from sklearn such as Logistic Regression from sklearn.linear_model, train_test_split from sklearn.model_selection, TfidfVectorizer from sklearn.feature_extraction.text, accuracy_score, confusion_matrix, classification_report from sklearn.metrics etc.

# Model

The model I am using is Logistic Regression due to its classification capabilities. I am using a test sample size of 20% while the remaining 80% is used for training. I have imported Pipeline from sklearn.pipeline to easily handle vectorization by TF-IDF and Logistic Regression on its own instead of managing every middle step on my own.

# Result

The model achieved an accuracy of **89.56 %**.

# How to run the model

1) Ensure that pandas and scikit-learn libraries are installed. If they are not, run:
 
        pip install pandas scikit-learn

2) Make sure the dataset **IMDB-Dataset.csv** is present in the running directory.
3) Open **Sentiment_Analysis.ipynb** file.
4) Run the notebook cells in order.

# Example Prediction

**Input**

    new_review = ["This movie is fantastic."]
    new_sentiment = model.predict(new_review)
    
    print("The sentiment of this review is: ", new_sentiment[0])

**Output**

    The sentiment of this review is: positive 