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
- `label` → review type (`0 = genuine`, `1 = fake`)

### Steps performed:
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
  ```

- Evaluation metrics:
  - **Accuracy**
  - **Precision**
  - **Classification Report**

---

## 💻 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/nagapriya15/EML_PBL_Project.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Python script:
   ```bash
   python eml_pbl.py
   ```

*(Ensure `reviews.csv` is in the same directory as `eml_pbl.py`.)*

---

## 📊 Sample Output
```
Accuracy: 0.8947
Precision: 0.8800
Classification Report:
              precision    recall  f1-score   support

           0       0.91      0.89      0.90        80
           1       0.88      0.90      0.89        70

    accuracy                           0.89       150
   macro avg       0.89      0.89      0.89       150
weighted avg       0.89      0.89      0.89       150
```

---

## 🧾 Results
The model demonstrates strong performance in distinguishing fake and genuine reviews.  
You can improve it further by:
- Using **Word2Vec** or **BERT** embeddings  
- Trying **Random Forest** or **SVM** classifiers  
- Expanding your dataset for better generalization  

---

## 👩‍💻 Author
**Naga Priya**  
🎓 AI & ML Student | Passionate about NLP, Data Science & AI-driven automation  
