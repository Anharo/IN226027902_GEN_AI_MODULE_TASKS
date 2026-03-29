# 📊 Sentiment Analysis using NLP & Machine Learning

## 🚀 Overview

This project implements a complete end-to-end Sentiment Analysis system using Natural Language Processing (NLP) techniques and Machine Learning models. The goal is to classify text data into sentiment categories such as positive and negative.

The project covers the entire pipeline from raw text preprocessing to feature engineering, model training, evaluation, and comparison.

---

## 📂 Dataset

* Source: Kaggle
* Dataset Used: IMDb Movie Reviews Dataset
* The dataset contains textual reviews labeled as **positive** or **negative**.

---

## ⚙️ Pipeline Workflow

Raw Data → Preprocessing → Feature Engineering → Model Training → Evaluation → Comparison

---

## 🧹 NLP Preprocessing

The following preprocessing steps were applied:

* Lowercasing text
* Removing HTML tags
* Removing URLs
* Removing punctuation and special characters
* Tokenization
* Stopword removal
* Stemming

These steps help in cleaning the raw text and improving model performance.

---

## 🔢 Feature Engineering

Two techniques were used to convert text into numerical form:

### 1. Bag of Words (BoW)

* Counts frequency of words
* Simple and fast

### 2. TF-IDF

* Assigns importance to words
* Reduces impact of common words
* Generally performs better than BoW

---

## 🤖 Machine Learning Models

The following models were implemented:

* Logistic Regression
* Naive Bayes (MultinomialNB)
* Decision Tree Classifier

Each model was trained using both BoW and TF-IDF features.

---

## 📈 Model Evaluation

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

---

## 📊 Results & Insights

* TF-IDF outperformed Bag of Words in most cases.
* Logistic Regression achieved the best overall performance.
* Naive Bayes was fast and efficient but slightly less accurate.
* Decision Tree showed lower performance due to overfitting on sparse data.

---

## ⚠️ Limitations

* A subset of the dataset was used for faster computation.
* No hyperparameter tuning was applied.
* Advanced techniques like Word2Vec or deep learning were not implemented.

---

## 🔮 Future Improvements

* Use Word2Vec, GloVe, or BERT embeddings
* Apply hyperparameter tuning
* Implement deep learning models (LSTM, Transformers)
* Deploy as a web application

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* NLTK
* Scikit-learn
* Matplotlib, Seaborn

---

## 📌 How to Run

1. Clone the repository:

```bash
git clone https://github.com/Anharo/IN226027902_GEN_AI_MODULE_TASKS.git
```

2. Run the notebook:

```bash
jupyter notebook
```

---

## 📎 Author

* Anish Sharma

---

## ⭐ If you like this project

Give it a star ⭐ on GitHub!
