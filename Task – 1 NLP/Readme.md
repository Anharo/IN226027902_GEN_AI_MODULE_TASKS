# 🧠 Text Preprocessing & NLP Pipeline

## 📌 Overview

This project implements a complete **text preprocessing pipeline** in Python, covering cleaning, normalization, tokenization, analytics, and robustness handling.

It is designed as a foundational step for NLP tasks such as:

* Sentiment Analysis
* Text Classification
* Information Retrieval
* Machine Learning pipelines

---

## ⚙️ Features

### ✅ Text Cleaning

* Convert text to lowercase
* Remove numbers
* Remove URLs and email patterns
* Remove punctuation and emojis
* Remove extra spaces

### ✅ Normalization

* Handle repeated characters
  *(e.g., "soooo" → "so")*

### ✅ Token Processing

* Tokenization (word splitting)
* Remove short tokens (≤ 2 characters)
* Preserve important words like **"no"** and **"not"**

### ✅ Analytics

* Token count per sentence
* Unique token count
* Average token length
* Frequency analysis using `Counter`

### ✅ Robust Error Handling

Handles edge cases like:

* Empty strings
* Only emojis
* Only numbers
* Invalid inputs (e.g., `None`)

---

## 📂 Project Structure

```
project/
│── GENAI_TASK_1.ipynb     
│── README.md
```

---

## 🚀 Usage

### 1. Import Functions

```python
from preprocess import preprocess_text
from pipeline import full_pipeline
```

---

### 2. Example Input

```python
text_list = [
    "Get 100% FREE access now!!!",
    "I absolutely looooved this product 😍😍",
    "Visit https://openai.com now!"
]
```

---

### 3. Run Pipeline

```python
result = full_pipeline(text_list)

print(result["tokens"])
print(result["clean_sentences"])
```

---

## 📦 Output Format

```python
{
    "tokens": ["get", "free", "access", "now", ...],
    "clean_sentences": [
        "get free access now",
        "absolutely loved this product",
        "visit now"
    ]
}
```

---

## 📊 Token Analytics

Using `collections.Counter`:

```python
from collections import Counter

counter = Counter(result["tokens"])

print(counter.most_common(10))  # Top words
```

---

## 🔍 Key NLP Concepts

### 🔤 Case Sensitivity

* "Love" vs "love" → normalized to same token after lowercasing

### 🚫 Stopwords

* Removing stopwords reduces noise
* But may harm:

  * Sentiment ("not good")
  * Queries ("who", "where")

### 🌱 Stemming vs Lemmatization

| Technique     | Output              | Accuracy            |
| ------------- | ------------------- | ------------------- |
| Stemming      | "studies" → "studi" | Fast, less accurate |
| Lemmatization | "studies" → "study" | Accurate, slower    |

---

## ⚠️ Limitations

* Does not preserve emojis (can carry sentiment)
* No stemming/lemmatization applied
* Basic regex-based cleaning (not language-aware)

---

## 🔮 Future Improvements

* Add stemming / lemmatization (NLTK / spaCy)
* Emoji sentiment handling 😊
* Stopword customization
* TF-IDF / embeddings integration
* ML model integration

---

## 🧪 Testing

The pipeline is tested on:

* Emojis
* Numbers
* URLs
* Repeated characters
* Mixed case text

---

## 📌 Example

**Input:**

```
"I am not happy with this!!! 😡"
```

**Output:**

```
Tokens: ['not', 'happy', 'with', 'this']
Cleaned: "not happy with this"
```

---

## 👨‍💻 Author

Built as part of an NLP learning project 🚀

---
