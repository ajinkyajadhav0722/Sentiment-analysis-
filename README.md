# Sentiment Analysis of Amazon Alexa Reviews

## Overview
This project implements a sentiment analysis system on Amazon Alexa reviews to classify feedback as positive or negative. By leveraging machine learning techniques, we aimed to provide actionable insights from customer reviews while achieving high prediction accuracy.

---

## Objectives
1. Classify reviews as **positive** (feedback = 1) or **negative** (feedback = 0).
2. Train and tune machine learning models for maximum performance.
3. Extract trends and insights from the data for better product understanding.

---

## Dataset
The dataset contains 5 key features:
- **Rating**: Customer rating (1-5).
- **Date**: Review date.
- **Variation**: Product variation (e.g., Charcoal Fabric).
- **Verified Reviews**: Customer reviews.
- **Feedback**: Target variable (1 = Positive, 0 = Negative).

---

## Workflow

### 1. Data Preprocessing
- Removed null values.
- Created a new feature, `length`, to capture the length of each review.
- Cleaned reviews using **PorterStemmer** for stemming and removed stopwords.
- Vectorized text data using `CountVectorizer`.

### 2. Exploratory Data Analysis
- **Distribution of Ratings and Feedback**:
  - ~91.87% of feedback was positive.
  - Wordclouds revealed frequent words for positive and negative reviews.
- **Trends**:
  - Longer reviews often indicated dissatisfaction.
  - Variations like "Walnut Finish" had higher ratings.

### 3. Modeling
- Implemented and evaluated the following models:
  1. **Random Forest Classifier**:
     - Training Accuracy: **99.4%**
     - Testing Accuracy: **94.2%**
     - Tuned using GridSearchCV for optimal parameters.
  2. **XGBoost Classifier**:
     - Training Accuracy: **97.1%**
     - Testing Accuracy: **94.1%**
  3. **Decision Tree Classifier**:
     - Training Accuracy: **99.4%**
     - Testing Accuracy: **91.5%**

### 4. Deployment
- Saved models and preprocessing tools using `pickle` for reuse.

---

## Results
| Model                     | Training Accuracy | Testing Accuracy | Remarks                          |
|---------------------------|-------------------|------------------|----------------------------------|
| Random Forest Classifier  | 99.4%            | 94.2%            | Best overall performance         |
| XGBoost Classifier        | 97.1%            | 94.1%            | Competitive but slightly slower  |
| Decision Tree Classifier  | 99.4%            | 91.5%            | Simple but less robust           |

---

## Insights
1. **Positive Reviews**:
   - Praised device usability and voice recognition.
2. **Negative Reviews**:
   - Highlighted sound quality and technical glitches.
3. **Product Variations**:
   - "Walnut Finish" had the highest mean rating.

---

## Technologies Used
- **Python Libraries**:
  - `pandas`, `numpy`, `seaborn`, `matplotlib`: For EDA.
  - `nltk`: For text preprocessing.
  - `sklearn`: For modeling.
  - `xgboost`: For advanced modeling.
  - `wordcloud`: For visualizing frequent words.
- **Machine Learning Models**:
  - Random Forest, XGBoost, Decision Tree.

---

## File Structure
