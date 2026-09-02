# SMS Spam Detection using Machine Learning

## Overview

SMS spam is a common problem where unwanted, promotional, fraudulent, or potentially harmful messages are sent to users. Manually identifying these messages can be difficult, especially when dealing with a large number of incoming messages.

This project develops a **Machine Learning-based SMS Spam Detection system** that automatically classifies messages into two categories:

* **Ham** – Legitimate or normal messages
* **Spam** – Unwanted, promotional, suspicious, or fraudulent messages

The project uses **Natural Language Processing (NLP)** to transform text messages into numerical features and applies multiple supervised machine learning algorithms to identify the best-performing classification model.

The complete workflow covers data preprocessing, exploratory analysis, text feature extraction, model training, evaluation, model comparison, and prediction of new SMS messages.

---

## Problem Statement

With the increasing use of SMS communication, users frequently receive unwanted promotional messages, fake offers, suspicious links, and fraudulent notifications. An automated system is therefore useful for identifying potentially unwanted messages before they reach the user.

The objective of this project is to build a classification model capable of learning patterns from previously labeled SMS messages and predicting whether a new message is **Spam or Ham**.

---

## Technologies and Libraries

The project was developed using Python and the following libraries:

* **Pandas** – Data loading and manipulation
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Scikit-learn** – Machine learning and evaluation
* **Jupyter Notebook** – Development and experimentation

---

## Text Feature Extraction

Machine learning algorithms cannot directly process raw text. Therefore, the SMS messages were converted into numerical representations using **TF-IDF (Term Frequency-Inverse Document Frequency)**.

TF-IDF assigns importance to words based on how frequently they occur within a message while considering how common they are across the complete collection of messages.

The project uses:

* Lowercase conversion
* English stop-word removal
* Unigrams and bigrams
* Maximum of 5,000 features

```python
TfidfVectorizer(
    lowercase=True,
    stop_words="english",
    ngram_range=(1, 2),
    max_features=5000
)
```

Using both unigrams and bigrams allows the model to capture individual words as well as meaningful two-word combinations.

---

## Models Implemented

Three different classification algorithms were trained and evaluated.

### 1. Logistic Regression

Logistic Regression is a commonly used classification algorithm that estimates the probability of a sample belonging to a particular class.

In this project, it is used to classify TF-IDF representations of SMS messages into Ham or Spam.

### 2. Multinomial Naive Bayes

Multinomial Naive Bayes is particularly suitable for text classification problems because it works effectively with word-frequency and TF-IDF-based representations.

It provides a fast and efficient approach for detecting patterns commonly associated with spam messages.

### 3. Linear Support Vector Machine

LinearSVC is a Support Vector Machine algorithm designed for classification. It attempts to find an optimal decision boundary that separates the different classes.

It is particularly effective for high-dimensional text data, where TF-IDF can produce thousands of features.

---

## Prediction on New Messages

The project includes functionality for testing the trained model on new SMS messages.

A new message is first transformed using the same TF-IDF vectorizer used during training. The resulting numerical representation is then passed to the selected machine learning model.

Example:

```text
Input:
Congratulations! You have won a free prize. Claim it now!

Prediction:
SPAM
```

Another example:

```text
Input:
Hey, are we meeting at 5 PM today?

Prediction:
HAM
```

This demonstrates how the trained model can be used for real-world text classification.

---

## Conclusion

This project demonstrates how **Natural Language Processing and Machine Learning can be combined to automatically detect SMS spam**.

By converting text messages into numerical features using TF-IDF and comparing multiple classification algorithms, the project provides a practical approach to binary text classification.

The project also demonstrates an important real-world machine learning workflow — from **raw data and preprocessing to feature engineering, model training, evaluation, comparison, and prediction**.

Overall, this project strengthened my understanding of **NLP, text classification, supervised machine learning, model evaluation, and practical ML workflow implementation**.

---

## Author

**Varsha A**

B.Sc. Artificial Intelligence & Machine Learning
Aspiring Machine Learning / Data Science Professional
