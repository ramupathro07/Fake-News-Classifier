# 📰 Fake News Classification using Machine Learning

## 📌 Project Overview

This project aims to classify news articles as **Fake News** or **Real News** using Natural Language Processing (NLP) and Machine Learning techniques. The model analyzes news headlines, preprocesses textual data, and predicts whether the news content is trustworthy or misleading.

---

# 🎯 Problem Statement

The rapid spread of fake news through digital platforms can influence public opinion, create misinformation, and impact decision-making. Manually verifying news is time-consuming and inefficient.

This project builds a Machine Learning model that automatically identifies fake news articles based on their titles.

---

# 💼 Business Objective

- Detect fake news automatically.
- Reduce misinformation spread.
- Improve content verification processes.
- Assist media organizations and fact-checking platforms.
- Enhance trust in online information.

---

# 📊 Dataset Information

### Dataset Features

| Feature | Description |
|----------|-------------|
| id | Unique identifier |
| title | News headline/title |
| author | Author name |
| text | News content |
| label | Target variable (0 = Real, 1 = Fake) |

### Target Variable

- **0 → Real News**
- **1 → Fake News**

---

# 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- Scikit-Learn
- Jupyter Notebook

---

# 🔄 Machine Learning Workflow

```text
Data Collection
      ↓
Data Cleaning
      ↓
Text Preprocessing
      ↓
Feature Extraction (Bag of Words)
      ↓
Train-Test Split
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Prediction
```

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed:

### Data Cleaning

- Removed unnecessary columns (`id`)
- Removed missing values
- Reset dataframe index

### Text Preprocessing

- Converted text to lowercase
- Removed special characters
- Tokenization
- Stopword removal
- Stemming using Porter Stemmer

### NLP Techniques Used

- Bag of Words (BoW)
- N-Grams (1 to 3)
- Count Vectorization

```python
CountVectorizer(max_features=5000, ngram_range=(1,3))
```

---

# 📈 Exploratory Data Analysis (EDA)

### Analysis Performed

- Dataset shape analysis
- Feature inspection
- Missing value detection
- Target class distribution visualization

### Insights

- Distribution of Fake and Real news articles.
- Text data requires extensive cleaning before modeling.
- Balanced dataset improves model reliability.

---

# 🤖 Models Implemented

## 1️⃣ Multinomial Naive Bayes

### Why Used?

- Performs well on text classification tasks.
- Fast and efficient for large textual datasets.
- Works effectively with Bag-of-Words features.

---

## 2️⃣ Logistic Regression

### Why Used?

- Strong baseline classification algorithm.
- Handles high-dimensional text data efficiently.
- Produces highly interpretable results.

---

# ✂️ Train-Test Split

```python
train_test_split(
    X,
    y,
    test_size=0.20,
    random_state=0
)
```

### Split Ratio

- Training Data → 80%
- Testing Data → 20%

---

# 📏 Evaluation Metrics

The following metrics were used:

### Accuracy

Measures overall correctness.

```text
Accuracy = Correct Predictions / Total Predictions
```

### Precision

Measures how many predicted fake news articles were actually fake.

```text
Precision = TP / (TP + FP)
```

### Recall

Measures how many actual fake news articles were correctly identified.

```text
Recall = TP / (TP + FN)
```

### Confusion Matrix

Used to visualize:

- True Positives
- True Negatives
- False Positives
- False Negatives

---

# ⚙️ Hyperparameter Tuning

### Multinomial Naive Bayes

Tuned:

```python
alpha = 0.1 to 1.0
```

### Logistic Regression

Tuned:

```python
C = 0.1 to 1.0
```

Best-performing parameters were selected based on accuracy scores.

---

# 📊 Model Comparison

| Model | Purpose |
|---------|----------|
| Multinomial Naive Bayes | Text Classification |
| Logistic Regression | Binary Classification |

Both models were trained and evaluated on the same dataset.

---

# 🔍 Prediction System

A custom prediction function was developed to classify user-provided news headlines.

### Prediction Pipeline

```text
Input News
      ↓
Cleaning
      ↓
Tokenization
      ↓
Stopword Removal
      ↓
Stemming
      ↓
Vectorization
      ↓
Model Prediction
      ↓
Fake / Real
```

### Example

```python
fake_news("Breaking: Government announces new policy")
```

Output:

```text
Prediction: REAL NEWS
```

or

```text
Prediction: FAKE NEWS
```

---

# 📂 Project Structure

```text
Fake-News-Classifier/
│
├── data/
│   ├── kaggle_fake_train.csv
│   └── kaggle_fake_test.csv
│
├── notebooks/
│   └── Fake News Classifier.ipynb
│
├── images/
│   ├── class_distribution.png
│   └── confusion_matrix.png
│
├── README.md
│
└── requirements.txt
```

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Fake-News-Classifier.git
```

Move into project directory:

```bash
cd Fake-News-Classifier
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run Jupyter Notebook:

```bash
jupyter notebook
```

---

# 📦 Required Libraries

```bash
pip install numpy
pip install pandas
pip install matplotlib
pip install seaborn
pip install nltk
pip install scikit-learn
```

---

# 🎯 Key Learnings

- Natural Language Processing fundamentals
- Text preprocessing techniques
- Feature extraction using Bag of Words
- Machine Learning model training
- Hyperparameter tuning
- Model evaluation metrics
- Fake News Detection systems

---

# 🔮 Future Enhancements

- TF-IDF Vectorization
- Word Embeddings (Word2Vec)
- LSTM / RNN Models
- BERT-based Transformer Models
- Flask/FastAPI Deployment
- Streamlit Web Application
- Real-Time News Verification API

---

# 📸 Results

### Visualizations Included

✅ Class Distribution Plot

✅ Confusion Matrix

✅ Model Performance Evaluation

---

# 🏆 Conclusion

This project successfully demonstrates how Natural Language Processing and Machine Learning can be used to identify fake news articles. By applying text preprocessing, feature extraction, and classification algorithms, the system can automatically distinguish between fake and real news with high effectiveness.

---

## 👨‍💻 Author

**Ramu Patro**

Aspiring Data Scientist | Machine Learning Enthusiast | Data Analyst

- GitHub: (https://github.com/ramupathro07)
- LinkedIn: www.linkedin.com/in/patro-ramu-0b2587231

⭐ If you found this project useful, consider giving it a star.
