# Sentiment Analysis on Text Data (NLP Project)

##  📌  Project Overview
This project builds an **end-to-end Natural Language Processing (NLP) pipeline** to classify text sentiment (**Positive vs Negative**) from unstructured textual data. The objective is to automatically analyze opinions and emotions expressed in text at scale.

The workflow includes data exploration, cleaning, TF-IDF feature extraction, and multi-class model training using Logistic Regression, Naive Bayes, and Linear SVC. Models are evaluated with accuracy, precision, recall, and macro F1-score, with special focus on minority classes.

The solution enables organizations to monitor sentiment trends, filter ambiguous content, and prioritize responses, supporting faster, data-driven decision-making while maintaining a robust, leakage-free modeling pipeline.

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
   - Stopwords & punctuation removal
   - Lowercasing  

4. **Modeling & Evaluation**  
   - Baseline model: **Logistic regression**  
   - Metrics: Accuracy, Precision, Recall, Macro F1 and Weighted F1  

---

##  📊  Results

| Model                   | Accuracy   | Precision (macro) | Recall (macro) | Macro F1   | Weighted F1 | Notes                                           |
| ----------------------- | ---------- | ----------------- | -------------- | ---------- | ----------- | ----------------------------------------------- |
| **Linear SVC ⭐**        | **67.14%** | **0.5646**        | **0.5680**     | **0.5626** | **0.6664**  | Best overall balance, strong minority handling  |
| Logistic Regression     | 64.77%     | 0.5315            | 0.5512         | 0.5337     | 0.6195      | Solid baseline, weaker minority recall          |
| Multinomial Naïve Bayes | 64.77%     | 0.5631            | 0.5012         | 0.5197     | 0.6546      | Strong on majority class, biased toward neutral |


**Interpretation:**  
- **Linear SVC** achieved the highest Macro-F1 score (0.5626), indicating the best balanced performance across all sentiment classes, including minority classes.
- **Multinomial NB** had slightly lower macro F1 but still performed competitively.  
- **Logistic Regression** provided a reasonable baseline but was outperformed by the other models.

---

##  💡  Key Insights
**Class Distribution**: Most tweets are neutral or positive, with negative sentiments being less frequent.

**Model Performance**:

- Linear SVC achieved the best accuracy and F1 score.

- Logistic Regression and Multinomial Naive Bayes also performed well as baseline models.

- Feature Importance: TF-IDF features (words and bigrams) effectively captured sentiment cues.

**Data Cleaning Impact**: Lowercasing, removing noise (URLs, mentions, punctuation), tokenization, stopword removal, and lemmatization improved model accuracy significantly.

---
## 🧩  Challenges
    -Strong class imbalance (neutral dominates)

    -Overlapping language between neutral & positive

    -Minority class detection (negative sentiment)


## ✨ Recommendations
1. Address class imbalance using oversampling, undersampling, or class-weighted models.

2. Explore advanced embeddings (BERT, RoBERTa) for capturing subtle semantic nuances.

3. Continuously update the model with new data to maintain performance.

4. Perform error analysis on misclassified tweets to improve preprocessing and model accuracy.

5. Deploy the model via an API for real-time sentiment monitoring and dashboards.

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
