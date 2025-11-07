# 🧠 Fake vs Genuine Review Classification (EML_PBL Project)

## 📘 Project Overview
This project aims to classify online product reviews as **genuine** or **fake** using **Natural Language Processing (NLP)** and **Machine Learning** techniques.  
By analyzing text patterns, the model helps detect fraudulent reviews that can mislead consumers and affect business credibility.

---

## ⚙️ Technologies & Libraries Used
- 🐍 **Python 3**
- 📦 **Libraries:**
  - `pandas` — Data manipulation and preprocessing  
  - `re` — Regular expressions for text cleaning  
  - `nltk` — Stopword removal and lemmatization  
  - `scikit-learn` — Model building and evaluation  
  - `TfidfVectorizer` — Text feature extraction  
  - `LogisticRegression` — Classification algorithm  

---

## 🧹 Data Preprocessing
The dataset (e.g., `reviews.csv`) must contain:
- `review_text` → the review content  
- `label` → review type (`0` = genuine, `1` = fake)

Steps performed:
1. Converted text to lowercase  
2. Removed special characters and punctuation  
3. Removed stopwords using NLTK  
4. Applied **WordNet Lemmatizer**  
5. Encoded labels if categorical  

---

## 🤖 Model Training
The model uses **Logistic Regression** for binary classification.  
- Data split: **80% training / 20% testing**  
- Text transformed using **TF-IDF Vectorizer**  
- Model trained using:
  ```python
  model = LogisticRegression(max_iter=1000)
