# Sentiment Analysis on Text Data (NLP Project)

##  📌  Project Overview
This project builds an **end-to-end Natural Language Processing (NLP) pipeline** to classify text sentiment (**Positive vs Negative**) from unstructured textual data. The objective is to automatically analyze opinions and emotions expressed in text at scale.

The notebook follows the complete data science workflow: **problem definition, exploratory data analysis, text preprocessing, feature engineering, model training, and evaluation**, with special attention to **class imbalance**.

---

## ❓  Problem Statement
Analyzing large volumes of textual data manually is inefficient and error-prone. This project addresses the challenge of **automated sentiment classification** while handling **imbalanced sentiment classes**, where positive samples significantly outnumber negative ones.

---

##  🎯 Objectives
- Understand sentiment distribution and class imbalance  
- Clean and preprocess raw text data  
- Convert text into numerical representations using **TF-IDF**  
- Build a baseline **Naive Bayes** sentiment classifier  
- Evaluate model performance using standard classification metrics  
- Identify limitations and opportunities for improvement  

---

##  🛠️ Methodology
1. **Exploratory Data Analysis (EDA)**  
   - Sentiment class distribution  
   - Text length and word count analysis  

2. **Text Preprocessing**  
   - Lowercasing text  
   - Removing punctuation and stopwords  
   - Tokenization and normalization  

3. **Feature Engineering**  
   - TF-IDF vectorization  
   - Unigrams, bigrams, and trigrams  

4. **Modeling & Evaluation**  
   - Baseline model: **Naive Bayes**  
   - Metrics: Accuracy, Precision, Recall, F1-score  

---

##  📊  Results

| Model               | Precision (macro) | Recall (macro) | Macro F1 | Weighted F1 |
|---------------------|------------------|----------------|----------|-------------|
| Logistic Regression | 0.5315           | 0.5512         | 0.5337   | 0.6195      |
| Multinomial NB      | 0.5631           | 0.5012         | 0.5197   | 0.6546      |
| Linear SVC          | 0.5646           | 0.5680         | 0.5626   | 0.6664      |

**Interpretation:**  
- **Linear SVC** achieved the highest Macro-F1 score (0.5626), indicating the best balanced performance across all sentiment classes, including minority classes.
- **Multinomial NB** had slightly lower macro F1 but still performed competitively.  
- **Logistic Regression** provided a reasonable baseline but was outperformed by the other models.

---

##  💡  Key Insights
- Class imbalance significantly impacts negative sentiment recall  
- N-grams improve contextual understanding compared to unigrams alone  
- Naive Bayes provides a strong baseline but has limitations with minority classes  

---

## ✨ Recommendations
- Apply class imbalance techniques (SMOTE, resampling, or class weighting)  
- Experiment with advanced models (Logistic Regression, SVM, or BERT-based models)  
- Perform deeper error analysis on misclassified samples  
- Extend the model for real-time sentiment monitoring  

---

##  🧰  Tech Stack
| Languages & Core | Libraries & Tools |
|:--- |:--- |
| • **Python** | • **NLTK / SpaCy** |
| • **Pandas, NumPy** | • **Matplotlib, Seaborn** |
| • **Scikit-learn** | • **Jupyter Notebook** |

---

##  👥 Authors
| Name | GitHub Profile |
|------|----------------|
| **Sharon Kipruto** | [Sharon](https://github.com/sharonkipruto-code) |
| **Lorena Terah**   | [Lorena](https://github.com/lorenaterah) |
| **Edgar Owuor**    | [Edgar](https://github.com/edgarowuor-tech) |
| **Dawa Jarso**     | [Dawa](https://github.com/Dawa-Jarso) |
