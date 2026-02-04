# NLP Sentiment Analysis Project

## Project Overview
This project applies **Natural Language Processing (NLP)** and **machine learning** techniques to analyze sentiment expressed in tweets about brands and products.  
The goal is to classify whether a tweet expresses **positive, negative, or neutral sentiment** toward a brand or product, and to understand the linguistic patterns behind these sentiments.

The project follows a structured data science workflow, from business understanding to model interpretation.

---

## Business Understanding
Brands receive large volumes of customer feedback on social media but manually analyzing sentiment is inefficient and error-prone.  
This project helps automate sentiment detection, enabling businesses to:
- Track customer perception of products and brands
- Identify negative feedback early
- Understand drivers of positive and negative sentiment

---

## Data Understanding
- **Dataset size:** ~9,000 tweets  
- **Key columns:**
  - `tweet_text` – text content of tweets
  - `emotion_in_tweet_is_directed_at` – product/brand referenced
  - `is_there_an_emotion_directed_at_a_brand_or_product` – sentiment label

### Initial Observations
- Missing values in some columns
- Duplicate tweets present
- Class imbalance in sentiment labels
- Majority of tweets are not directed at a specific brand (“General”)

---

## Data Cleaning & Preprocessing
Key steps included:
- Renaming columns for readability
- Removing duplicates to prevent data leakage
- Handling missing values (dropping or imputing where appropriate)
- Text preprocessing:
  - Lowercasing
  - Tokenization
  - Stopword removal
  - Lemmatization
- Combining sentiment classes into **positive**, **negative**, and **neutral**

---

## Exploratory Data Analysis (EDA)
The analysis explored:
- Sentiment class distribution and imbalance
- Tweet length and word count by sentiment
- Frequently occurring words in positive vs negative tweets
- Brand/product distribution across tweets

**Key Insight:**  
Neutral tweets dominate the dataset, which required careful evaluation of model performance beyond accuracy alone.

---

## Feature Engineering
- Text vectorization using:
  - **Bag of Words**
  - **TF-IDF**
- Train-test split performed after preprocessing to avoid leakage

---

## Modeling
Multiple models were trained and evaluated, including:
- Naive Bayes
- Logistic Regression
- Tree-based models

The `lorena.ipynb` notebook focuses primarily on:
- Model training
- Hyperparameter tuning
- Performance comparison

---

## Evaluation Metrics
Given class imbalance, the following metrics were emphasized:
- Precision
- Recall
- F1-Score
- Confusion Matrix

Accuracy alone was not used as the primary success metric.

---

## Model Interpretation
- Feature importance analysis
- Inspection of words contributing most to positive and negative predictions
- Discussion of model generalization performance

---

## Repository Structure
```text
├── Sharon.ipynb     # Full NLP pipeline: EDA, preprocessing, modeling
├── lorena.ipynb     # Focused modeling and evaluation
── lorena.ipynb
├── README.md        # Project documentation
