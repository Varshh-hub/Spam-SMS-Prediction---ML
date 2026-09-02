#  SMS Spam Detection using Machine Learning

An NLP-based machine learning system that automatically classifies SMS messages as **Spam** or **Ham** using TF-IDF feature extraction and multiple supervised classification algorithms.

---

##  Overview

SMS spam is a common problem where users receive unwanted promotional messages, fraudulent offers, suspicious links, and potentially harmful notifications.

This project develops a **Machine Learning-based SMS Spam Detection system** that automatically classifies incoming messages into two categories:

*  **Ham** — Legitimate or normal messages
*  **Spam** — Unwanted, promotional, suspicious, or fraudulent messages

The project follows a complete machine learning workflow, starting from text preprocessing and exploratory analysis through feature extraction, model training, evaluation, model comparison, and prediction on new SMS messages.

---

##  Problem Statement

With the increasing use of SMS communication, users frequently receive unwanted promotional content, fake offers, suspicious links, and fraudulent notifications.

The objective of this project is to develop a machine learning classification system that can learn patterns from previously labeled SMS messages and predict whether a new message is **Spam or Ham**.

---

##  Machine Learning Models

Three supervised classification algorithms were implemented and compared.

### 1. Logistic Regression

Logistic Regression is a widely used classification algorithm that estimates the probability of a sample belonging to a particular class.

In this project, it is used to classify TF-IDF representations of SMS messages into **Spam** or **Ham**.

### 2. Multinomial Naive Bayes

Multinomial Naive Bayes is well suited for text classification tasks and is commonly used with word-based feature representations.

It provides a fast and efficient approach for identifying patterns associated with spam messages.

### 3. Linear Support Vector Machine

**LinearSVC** is a Support Vector Machine algorithm designed for classification.

It finds a decision boundary that separates different classes and performs particularly well on high-dimensional text data such as TF-IDF representations.

---

##  Model Performance

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score

| Model                   |   Accuracy | Precision | Recall |   F1 Score |
| ----------------------- | ---------: | --------: | -----: | ---------: |
| Logistic Regression     | **94.27%** |    95.42% | 77.80% |     85.71% |
| Multinomial Naive Bayes | **95.04%** |    89.31% | 88.13% |     88.72% |
| Linear SVM              | **95.38%** |    92.65% | 85.93% | **89.17%** |

###  Best Performing Model

Based on the evaluation results, **Linear Support Vector Machine** achieved the highest overall performance with:

> **95.38% Accuracy and 89.17% F1 Score**

The F1 Score is particularly useful for this classification problem because it considers both **Precision and Recall**, which are important when identifying spam messages.

---

##  Prediction on New Messages

The trained model can be used to classify previously unseen SMS messages.

Before prediction, the new message is transformed using the **same TF-IDF vectorizer fitted during training**.

### Example 1 — Spam

**Input:**

```text
Congratulations! You have won a free prize. Claim it now!
```

**Prediction:**

```text
SPAM
```

### Example 2 — Ham

**Input:**

```text
Hey, are we meeting at 5 PM today?
```

**Prediction:**

```text
HAM
```

---

##  Results & Insights

The experiments demonstrate that traditional machine learning algorithms can perform effectively on text classification problems when combined with appropriate NLP feature engineering.

Among the three tested models:

* Logistic Regression achieved **94.27% accuracy**
* Multinomial Naive Bayes achieved **95.04% accuracy**
* Linear SVM achieved the highest accuracy of **95.38%**
* Linear SVM also achieved the highest F1 Score of **89.17%**

These results show the effectiveness of **TF-IDF + supervised machine learning** for SMS spam detection.

---

## 🎓 What I Learned

This project strengthened my practical understanding of:

* **Natural Language Processing**
* **Text preprocessing**
* **TF-IDF feature engineering**
* **Binary text classification**
* **Supervised machine learning**
* **Model evaluation**
* **Precision, Recall, and F1 Score**
* **Comparing multiple ML algorithms**
* **End-to-end machine learning workflow**

It also provided hands-on experience in taking a machine learning problem from **raw text data to a working prediction system**.

---

## 👩‍💻 Author

### Varsha A

AI & ML Graduate | Junior Data Scientist & Machine Learning Engineer | Python | SQL | Excel | Power BI | Prompt Engineer | Front-End Developer
