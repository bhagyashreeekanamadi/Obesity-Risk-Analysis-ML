# Obesity Analysis Using Machine Learning

## 📌 Project Overview

This project demonstrates an end-to-end Machine Learning workflow using an obesity dataset.

The project covers:

* Data Understanding
* Data Cleaning
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Regression
* Classification
* Unsupervised Learning
* Model Evaluation
* Cluster Analysis
* PCA Visualization

The same dataset is used to practice **Regression, Classification, and Clustering** techniques.

---

## 📊 Dataset

The project uses the **Obesity Dataset**, which contains demographic, lifestyle, eating-habit, physical-activity, and health-related information.

### Dataset Features

Some of the important features include:

* Age
* Gender
* Height
* Weight
* Family history of overweight
* Food consumption habits
* Water consumption
* Physical activity
* Transportation method
* Smoking
* Obesity level

### Target Variables

**Regression**

```text
Weight
```

Predict an individual's weight using the available demographic and lifestyle features.

**Classification**

```text
NObeyesdad
```

Predict the individual's obesity category.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# 🔎 Project Workflow

```text
Dataset
   ↓
Data Understanding
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
 ┌─────────────────┬──────────────────┬─────────────────┐
 │    Regression   │  Classification  │   Clustering    │
 ├─────────────────┼──────────────────┼─────────────────┤
 │ Linear Regression│ Logistic Regression│ K-Means       │
 │ Ridge Regression │ KNN               │ Elbow Method   │
 │ Lasso Regression │ Decision Tree     │ Silhouette     │
 │                  │ Random Forest     │ PCA            │
 └─────────────────┴──────────────────┴─────────────────┘
```

---

# 1. Data Understanding

The dataset is loaded and explored using:

* `head()`
* `info()`
* `describe()`
* `shape`
* `columns`
* `value_counts()`

The dataset is also checked for:

* Missing values
* Duplicate records
* Data types
* Potential outliers

---

# 2. Data Cleaning

Duplicate records are identified and removed.

The original dataset contains:

```text
2111 records
```

Duplicate records identified:

```text
24
```

After removing duplicates:

```text
2087 records
```

---

# 3. Exploratory Data Analysis

EDA is performed to understand patterns and relationships within the dataset.

### Numerical Analysis

* Distribution analysis
* Boxplots
* Histograms
* Outlier detection
* Correlation analysis

### Categorical Analysis

Relationships between categorical variables and obesity level are explored using:

* Count plots
* Cross-tabulations

Examples:

* Gender vs Obesity Level
* Lifestyle factors vs Obesity Level
* Transportation vs Obesity Level

---

# 4. Feature Engineering

Three additional features are created.

### BMI

```text
BMI = Weight / Height²
```

BMI represents weight relative to height.

### Lifestyle Score

A simple lifestyle score is created using selected lifestyle-related variables:

```text
lifestyle_score = FAVC + SMOKE + SCC
```

### Activity-Hydration Ratio

```text
activity_hydration_ratio = FAF / (CH2O + 1)
```

This combines physical activity and water consumption into a derived feature.

---

# 5. Regression

## 🎯 Objective

Predict **Weight** using demographic, lifestyle, and health-related features.

### Models Used

* Linear Regression
* Ridge Regression
* Lasso Regression

### Evaluation Metrics

* MAE
* MSE
* RMSE
* R² Score

### Results

| Model             |   MAE |  RMSE |     R² |
| ----------------- | ----: | ----: | -----: |
| Linear Regression | 1.773 | 2.324 | 0.9923 |
| Ridge Regression  | 1.771 | 2.322 | 0.9924 |
| Lasso Regression  | 1.807 | 2.405 | 0.9918 |

Actual vs predicted values are also visualized to evaluate regression performance.

---

# 6. Classification

## 🎯 Objective

Predict the obesity category using:

```text
NObeyesdad
```

### Models Used

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest

### Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score

### Results

| Model               | Accuracy | Precision | Recall | F1 Score |
| ------------------- | -------: | --------: | -----: | -------: |
| Logistic Regression |   90.67% |    90.55% | 90.67% |   90.55% |
| KNN                 |   81.58% |    80.97% | 81.58% |   80.26% |
| Decision Tree       |   96.41% |    96.40% | 96.41% |   96.40% |
| Random Forest       |   96.41% |    96.73% | 96.41% |   96.45% |

A confusion matrix is also generated for the Random Forest model.

---

# 7. Unsupervised Learning

## 🎯 Objective

Identify groups of individuals with similar characteristics without using the obesity target during clustering.

### Algorithm

**K-Means Clustering**

### Clustering Workflow

```text
Feature Selection
       ↓
Data Preprocessing
       ↓
Scaling + One-Hot Encoding
       ↓
K-Means
       ↓
Elbow Method
       ↓
Silhouette Score
       ↓
Cluster Profiling
       ↓
PCA Visualization
```

### Cluster Analysis

The clusters are analyzed using:

* Gender
* Transportation method
* Eating habits
* Obesity category
* Numerical feature averages

PCA is used to visualize the clusters in two dimensions.

---

# 🤖 Machine Learning Models

| Machine Learning Type | Models              |
| --------------------- | ------------------- |
| Regression            | Linear Regression   |
| Regression            | Ridge Regression    |
| Regression            | Lasso Regression    |
| Classification        | Logistic Regression |
| Classification        | KNN                 |
| Classification        | Decision Tree       |
| Classification        | Random Forest       |
| Clustering            | K-Means             |

---

# 📚 Concepts Practiced

This project provides hands-on practice with:

* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Feature Engineering
* Numerical Feature Scaling
* Categorical Feature Encoding
* Train/Test Split
* Regression
* Classification
* Clustering
* Model Evaluation
* Confusion Matrix
* Elbow Method
* Silhouette Score
* PCA

---

# 📁 Project Structure

```text
obesity-ml-project/
│
├── README.md
│
├── dataset/
│   └── ObesityDataSet_raw_and_data_sinthetic.csv
│
└── src/
    └── obesity_ml_analysis.ipynb
```

---

# 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
cd obesity-ml-project
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
src/obesity_ml_analysis.ipynb
```

Make sure the dataset path in the notebook points to:

```text
../dataset/ObesityDataSet_raw_and_data_sinthetic.csv
```

---

# 🔮 Future Improvements

Possible extensions to this project include:

* Hyperparameter tuning
* Cross-validation
* Feature importance analysis
* Model saving using Joblib
* FastAPI deployment
* Interactive dashboard
* Explainable AI using SHAP
* Model monitoring

---

# 👩‍💻 Author

**Bhagyashree Kanamadi**

Test Engineer | Python | Machine Learning | GenAI | AI Evaluation

### Data Sutra by Bhagyashree

AI • Data Science • Machine Learning

---

## ⭐ Project Summary

This project demonstrates a complete Machine Learning workflow using one real-world dataset across:

**Regression + Classification + Unsupervised Learning**

It combines data analysis, feature engineering, model development, evaluation, and clustering in a single practical project.
