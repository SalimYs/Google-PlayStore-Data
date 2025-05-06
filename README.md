# 📱 Google Play Store Data Analysis & ML Project

This project is a complete data science pipeline applied to the [Google Play Store dataset](https://www.kaggle.com/datasets/lava18/google-play-store-apps). It covers **data cleaning**, **exploratory data analysis (EDA)**, **feature engineering**, and a suite of **machine learning models** including **regression**, **classification**, and **clustering**.

> 🔍 Goal: Predict app ratings and uncover insights about factors that influence app success such as number of installs, reviews, size, and type.

---

## 📦 Dataset Overview

- **Source**: Kaggle ([Google Play Store Apps](https://www.kaggle.com/datasets/lava18/google-play-store-apps))
- **Rows**: ~10,000 apps
- **Features**: App name, Category, Rating, Reviews, Size, Installs, Type (Free/Paid), Price, Content Rating, etc.
- **Challenge**: Dataset had missing values, inconsistent formatting, and required extensive preprocessing.

---

## 🧹 Data Cleaning & Preprocessing

- Converted columns like `Reviews`, `Installs`, `Size`, and `Price` to proper numeric formats.
- Extracted features from `Last_Updated` (Year and Month).
- Replaced problematic values (e.g. “Varies with device”) with `NaN`, then imputed or removed.
- Encoded:
  - **Nominal features** using `HashingEncoder`
  - **Ordinal features** using `LabelEncoder`
- Removed outliers using Z-score filtering.

---

## 📊 Exploratory Data Analysis (EDA)

- Analyzed distributions of installs, reviews, and ratings.
- Created visualizations like:
  - Word cloud of most common app names
  - Top-rated and most-installed apps
  - Category distribution (bar and pie charts)
- Correlation heatmaps to identify influential features

---

## 🤖 Machine Learning Models

### 1. Regression
- **Goal**: Predict app ratings
- Models: Linear Regression, Random Forest Regressor
- **Result**: Regression scores were low, indicating the target (Rating) may not be ideal for regression.

### 2. Classification
- **Goal**: Predict integer-rounded ratings
- Models: Logistic Regression, SVM, Random Forest, Decision Tree, KNN, Gradient Boosting, AdaBoost, Extra Trees, Naive Bayes
- Best Accuracy:
  - **SVM & Logistic Regression**: ~77.5%
  - **Gradient Boosting**: ~77.3%
  - **Naive Bayes** performed poorly (~59%)

### 3. Clustering
- **Goal**: Group apps into meaningful segments
- Methods:
  - K-Means (with PCA for visualization)
  - Hierarchical Clustering
- **Best Result**: K-Means (4 clusters) with Silhouette Score ≈ 20.6%
- DBSCAN and Hierarchical clustering had lower quality clusters

---

## 📌 Key Learnings

- Deep understanding of EDA and data preparation
- Hands-on experience with a variety of models and encoders
- Learned to interpret results, evaluate models, and handle imbalanced & messy real-world data
- Importance of visual storytelling in data analysis

---

## 📁 Files

- `GoogleAppStoreData_work.ipynb`: Jupyter Notebook with full code and analysis

---

## 🚀 Future Work

- Try deep learning models or ensemble techniques
- Improve model interpretability
- Use NLP on app descriptions (if available) to enhance predictions

---

---

## 🏷️ Keywords

`Data Science` `EDA` `Google Play` `Machine Learning` `Clustering` `Classification` `Regression` `Python` `Sklearn` `Pandas` `Seaborn`

---

