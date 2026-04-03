# 🧠 BERT Fine-Tuning for Sentiment Analysis

## 📌 Project Overview

This project focuses on fine-tuning a pre-trained **BERT (Bidirectional Encoder Representations from Transformers)** model for sentiment classification using the **IMDB Movie Reviews dataset**.

The goal is to classify movie reviews as **positive** or **negative** by leveraging the contextual understanding of transformer-based models.

---

## 🎯 Objectives

* Understand how BERT works for text classification
* Perform fine-tuning using Hugging Face Transformers
* Apply tokenization using pre-trained models
* Evaluate performance using multiple metrics
* Conduct experiments and compare results

---

## 🛠️ Tech Stack

* Python 🐍
* PyTorch 🔥
* Hugging Face Transformers 🤗
* Scikit-learn 📊
* Matplotlib & Seaborn 📉

---

## 📂 Dataset

* **IMDB Movie Reviews Dataset**
* Binary classification:

  * 0 → Negative
  * 1 → Positive

---

## ⚙️ Pipeline

Raw Data → Preprocessing → Tokenization → Model Training → Evaluation → Comparison

---

## 🔹 Data Preprocessing

* Removed HTML tags and special characters
* Converted text to lowercase
* Removed stopwords (optional)
* Converted labels into numerical format

---

## 🔹 Tokenization

* Used `bert-base-uncased` tokenizer
* Applied padding and truncation
* Converted text into input IDs and attention masks

---

## 🔹 Model

* Pre-trained: `bert-base-uncased`
* Model: `AutoModelForSequenceClassification`
* Optimizer: AdamW
* Learning Rate: 2e-5

---

## 🔹 Training Details

* Epochs: 2
* Batch Size: 16
* Loss Function: CrossEntropyLoss (handled internally by BERT)

---

## 📊 Results

### 🔹 Performance Metrics

* **Accuracy:** 87%
* **Precision:** 0.87
* **Recall:** 0.87
* **F1 Score:** 0.87

---

### 🔹 Confusion Matrix

* True Negatives: 631
* False Positives: 137
* False Negatives: 69
* True Positives: 704

---

## 🧠 Analysis

* The model performs well with balanced precision and recall
* Slight bias toward predicting positive sentiment
* BERT captures contextual meaning effectively
* Misclassifications are relatively low

---

## 🧪 Experiments

### 🔸 1. Freezing BERT Layers

* Faster training
* Slight drop in accuracy

### 🔸 2. Fine-Tuning Last 2 Layers

* Better performance than freezing
* Reduced training time compared to full fine-tuning

---

## 🚀 Future Improvements

* Use **DistilBERT / RoBERTa**
* Apply learning rate scheduler
* Implement early stopping
* Increase training epochs

---

## 📁 Project Structure

```
📦 bert-sentiment-analysis
 ┣ 📜 notebook.ipynb
 ┣ 📜 README.md
```

---

## ▶️ How to Run

```bash
run jupyter notebook
```

---

## 🙌 Acknowledgment

This project was completed as part of an NLP assignment to understand transformer-based models and fine-tuning techniques.

---

⭐ If you found this project helpful, give it a star!
