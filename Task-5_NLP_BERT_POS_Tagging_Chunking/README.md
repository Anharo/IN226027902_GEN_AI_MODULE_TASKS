# 🚀 Fine-Tuning BERT for POS Tagging & Chunking

## 📌 Project Overview
This project demonstrates how to fine-tune a transformer model (BERT) for **token classification tasks**, specifically:
- Part-of-Speech (POS) Tagging
- Chunking (Phrase Detection)

The implementation follows a complete NLP pipeline including preprocessing, training, evaluation, and inference using Hugging Face Transformers.

---

## 🎯 Objective
- Build a token classification model using BERT
- Perform POS tagging and chunking
- Handle tokenization challenges (subwords & label alignment)
- Evaluate using sequence metrics (Precision, Recall, F1)

---

## 🛠️ Tech Stack
- Python
- Hugging Face Transformers
- Datasets
- PyTorch
- SeqEval
- Jupyter Notebook

---

## 📂 Dataset Used
**CoNLL-2003 Dataset**

### ✔ Features:
- Tokens
- POS Tags
- Chunk Tags
- Named Entity Tags

### ✔ Label Types:
- POS Tags → Grammar-based labels (e.g., NOUN, VERB)
- Chunk Tags → Phrase-based labels (e.g., NP, VP)

---

## 🔄 Pipeline Flow
```
Raw Data → Tokenization → Label Alignment → Model Training → Evaluation → Inference → Comparison
```

---

## ⚙️ Implementation Steps

### 1️⃣ Data Preprocessing
- Tokenization using BERT tokenizer
- Alignment of labels with tokens
- Handling:
  - Subwords
  - Special tokens ([CLS], [SEP])
  - Ignored labels (-100)

---

### 2️⃣ Model Setup
- Model: `bert-base-uncased`
- Used `AutoModelForTokenClassification`
- Configured:
  - `num_labels`
  - `id2label`
  - `label2id`

---

### 3️⃣ Training
- Trainer API from Hugging Face
- Key parameters:
  - Learning Rate: 2e-5
  - Epochs: 3
  - Batch Size: 16

---

### 4️⃣ Evaluation
Used **SeqEval** metric:
- Precision
- Recall
- F1 Score

---

### 5️⃣ Inference
Example:
```
Input: John works at Google in California
Output:
John → PROPN
works → VERB
at → ADP
Google → PROPN
in → ADP
California → PROPN
```

---

## 📊 Results
The model achieves strong performance due to contextual understanding of BERT.

- High accuracy on POS tagging
- Good phrase-level prediction for chunking

---

## ⚖️ Comparison: POS Tagging vs Chunking

| Feature | POS Tagging | Chunking |
|--------|------------|----------|
| Level | Word-level | Phrase-level |
| Difficulty | Easy | Medium |
| Purpose | Grammar | Structure |

---

## ⚠️ Challenges Faced
- Handling subword tokenization
- Aligning labels correctly
- Managing special tokens
- Device mismatch issues (CPU vs GPU)

---

## 💡 Observations
- BERT performs well due to contextual embeddings
- POS tagging is simpler than chunking
- Proper preprocessing significantly impacts performance

---

## 🧠 Key Learnings
- Token classification using transformers
- Importance of label alignment
- Using Trainer API efficiently
- Sequence evaluation using SeqEval

---

## ▶️ How to Run
```bash
pip install transformers datasets seqeval torch
```

Run the notebook:
```
jupyter notebook Task_5_NLP_BERT_POS_Tagging_Chunking.ipynb
```

---

## 📌 Future Improvements
- Use DistilBERT for faster training
- Hyperparameter tuning
- Deploy as an API

---

## 🔗 Submission
- Notebook: Included in repository
---

## 🙌 Acknowledgment
This project is part of an NLP learning assignment focused on practical transformer application