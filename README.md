# APR_Assignment1

## Titanic Survival Prediction using Logistic Regression

![Titanic Survival Prediction](https://placehold.co/800x300/000000/FFFFFF?text=Titanic+Survival+Prediction)

This project builds a logistic regression model to predict passenger survival on the RMS Titanic. The analysis is based on the Kaggle dataset, "**Titanic: Machine Learning from Disaster**."

---

## 📋 Table of Contents

- [Introduction](#introduction)
- [Methodology](#methodology)
- [Results](#results)
- [Potential Improvements](#potential-improvements)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)

---

## 📖 Introduction

The goal of this project is to apply fundamental machine learning concepts to a real-world dataset. We use passenger data—such as age, gender, and socio-economic class—to train a model that can classify whether a passenger survived the disaster.

---

## 🛠️ Methodology

The project follows a standard machine learning workflow:

1. **Data Exploration & Visualization**
    - Loaded the dataset and inspected its features (`Pclass`, `Sex`, `Age`, `Fare`, etc.).
    - Identified and quantified missing values in the `Age`, `Cabin`, and `Embarked` columns.
    - Visualized key relationships, confirming that gender and passenger class were strong indicators of survival.

2. **Data Preprocessing**
    - **Imputed Missing Values:** Filled missing `Age` data with the median age corresponding to the passenger's class (`Pclass`).
    - **Dropped Unnecessary Columns:** Removed `Cabin` (too many missing values), `Ticket`, and `Name` as they do not provide predictive value.
    - **Encoded Categorical Features:** Converted `Sex` and `Embarked` columns into numerical format using one-hot encoding.

3. **Model Training**
    - The data was split into an 80% training set and a 20% testing set.
    - A `LogisticRegression` model from scikit-learn was instantiated and trained on the preprocessed training data.

---

## 📊 Results

The model's performance was evaluated on the unseen test set, yielding the following results:

- **Overall Accuracy:** `82%`

### Classification Report

| Class                 | Precision | Recall | F1-Score | Support |
|-----------------------|-----------|--------|----------|---------|
| 0 (Did not Survive)   | 0.83      | 0.87   | 0.85     | 105     |
| 1 (Survived)          | 0.80      | 0.74   | 0.77     | 74      |

### Confusion Matrix

The model correctly identified 91 non-survivors and 55 survivors in the test set.

```
              Predicted
             |  0  |  1  |
---------------------------
Actual   0   |  91 |  14 |
         1   |  19 |  55 |
---------------------------
```

---

## 🚀 Potential Improvements

The current model serves as a strong baseline. Future work could include:

- **Feature Engineering:** Creating new features like `FamilySize` (from `SibSp` + `Parch`) or `IsAlone`.
- **Advanced Imputation:** Using more sophisticated techniques (e.g., KNN imputer) for missing `Age` values.
- **Alternative Models:** Experimenting with more complex algorithms like Random Forest, Gradient Boosting, or Support Vector Machines to potentially improve accuracy.

---

## ▶️ How to Run

Clone the repository:

```bash
git clone https://github.com/tanishkagupta2207/APR_Assignment1.git
```

```bash
Execute the cells
```
---

## 📦 Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

**Licensed by Google**
