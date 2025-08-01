# 📰 Fake News Detection System using Logistic Regression, Decision Tree, and Random Forest

This project aims to detect fake news using text classification techniques and multiple supervised machine learning models.

---

## ✅ 1. Text Vectorization: CountVectorizer & TF-IDF

To process textual news data, we use feature extraction techniques that convert text into numerical form:

### 🔸 CountVectorizer
- Converts text into a matrix of word counts.
- Example:
  - Sentences: `["fake news", "real news"]`
  - Vocabulary: `["fake", "news", "real"]`
  - Vectors:
    - "fake news" → `[1, 1, 0]`
    - "real news" → `[0, 1, 1]`
- Simple approach, but does not consider the importance or rarity of words.

### 🔸 TF-IDF (Term Frequency–Inverse Document Frequency)
- Weighs words based on their rarity across documents.
- Words that occur frequently in a document but rarely in the corpus get higher scores.
- Reduces the weight of common words like “the,” “is,” etc., giving more importance to contextually unique terms.

---

## ✅ 2. Machine Learning Models

### 🔸 Logistic Regression
- Used for **binary classification** tasks.
- Predicts the probability that a news article is fake or real.
- Lightweight and fast, but less effective for complex decision boundaries.

### 🔸 Decision Tree
- Splits data using a tree-like structure.
- Each node represents a decision based on a feature.
- Can easily overfit on training data if not properly tuned.

### 🔸 Random Forest
- An **ensemble** method using multiple Decision Trees.
- Trains on random subsets of data and features.
- Final prediction is based on majority voting.
- More robust and less prone to overfitting.
- **Achieved 99% accuracy** on our dataset.

---

## ✅ 3. Model Evaluation

### 🔸 Classification Report
Provides key performance metrics:
- **Precision** – Correctly predicted positives / All predicted positives.
- **Recall** – Correctly predicted positives / All actual positives.
- **F1-score** – Harmonic mean of precision and recall.
- **Accuracy** – Correct predictions / Total predictions.

### 🔸 Confusion Matrix
Summarizes model predictions vs actual labels:

|                 | Predicted Real      | Predicted Fake      |
|-----------------|---------------------|----------------------|
| **Actual Real** | True Negative (TN)  | False Positive (FP) |
| **Actual Fake** | False Negative (FN) | True Positive (TP)  |

### 🔸 Visualization
Used **Matplotlib** and **Seaborn** to:
- Plot the confusion matrix as a heatmap.
- Visualize classification report metrics for comparison.

---

## 📊 Final Results
- **Best Performing Model**: Random Forest
- **Accuracy**: 99%
- **Libraries Used**: `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`

---

## 📁 Dataset
- **Fake News Dataset** sourced from Kaggle.
- Consists of two CSV files: `Fake.csv` and `True.csv`.

---

## 🔧 Future Improvements
- Add more NLP preprocessing (lemmatization, n-grams).
- Try deep learning models (e.g., LSTM, BERT).
- Deploy the model via Flask or Streamlit for public use.

