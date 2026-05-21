# Fake News Classifier

A simple yet effective Machine Learning project to detect **Fake News** using NLP.

---

## Overview

This project analyzes news **titles** and classifies them as **Real** or **Fake**. It uses traditional text processing and two popular classification algorithms.

### Key Highlights:
- Text cleaning & stemming using NLTK
- Bag of Words feature extraction
- Trained with **Multinomial Naive Bayes** and **Logistic Regression**
- Achieved **93.63% accuracy** with Logistic Regression

---

## Results

| Model                    | Accuracy   |
|-------------------------|------------|
| Logistic Regression     | **93.63%** |
| Multinomial Naive Bayes | 90.59%     |

---

## Technologies Used
- Python
- Pandas, NumPy
- NLTK
- Scikit-learn
- Matplotlib & Seaborn

---

## Notebook Structure

| Section | Description |
|-------|-------------|
| **1. Libraries** | Import essential libraries (pandas, numpy, sklearn, nltk, etc.) |
| **2. Data Loading** | Load the training dataset (`kaggle_fake_train.csv`) |
| **3. Data Exploration** | Check shape, columns, sample data, and basic statistics |
| **4. Data Cleaning** | Drop unnecessary columns, handle missing values |
| **5. Visualization** | Count plot to see distribution of Real vs Fake news |
| **6. Text Preprocessing** | Clean titles (remove special chars, lowercase, remove stopwords, stemming) |
| **7. Feature Extraction** | Convert text into numerical features using Bag of Words (`CountVectorizer`) |
| **8. Model Building** | Train-test split |
| **9. Multinomial Naive Bayes** | Train, evaluate, confusion matrix, and hyperparameter tuning |
| **10. Logistic Regression** | Train, evaluate, confusion matrix, and hyperparameter tuning |
| **11. Final Model** | Train best model (Logistic Regression with C=0.8) |
| **12. Prediction** | Create function to predict on new news titles + testing on samples |

## How to Run

1. Clone the repository
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook "Fake News Classifier.ipynb"
   
## Run all cells   
#### Dataset
- kaggle_fake_train.csv – Training data
- kaggle_fake_test.csv – Test data

Made with ❤️ to help fight misinformation.
