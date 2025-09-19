# APR_Assignment1

Titanic Survival Prediction using Logistic Regression
!


Licensed by Google

(https://www.google.com/search?q=https://placehold.co/800x300/000000/FFFFFF%3Ftext%3DTitanic%2BSurvival%2BPrediction)

This project builds a logistic regression model to predict passenger survival on the RMS Titanic. The analysis is based on the classic Kaggle dataset, "Titanic: Machine Learning from Disaster."

📋 Table of Contents
Introduction

Methodology

Results

Potential Improvements

How to Run

Dependencies

📖 Introduction
The goal of this project is to apply fundamental machine learning concepts to a real-world dataset. We use passenger data—such as age, gender, and socio-economic class—to train a model that can classify whether a passenger survived the shipwreck. Logistic regression was chosen for its simplicity and effectiveness as a baseline model for binary classification.

🛠️ Methodology
The project follows a standard machine learning workflow:

Data Exploration & Visualization:

Loaded the dataset and inspected its features (Pclass, Sex, Age, Fare, etc.).

Identified and quantified missing values in the Age, Cabin, and Embarked columns.

Visualized key relationships, confirming that gender and passenger class were strong indicators of survival.

Data Preprocessing:

Imputed Missing Values: Filled missing Age data with the median age corresponding to the passenger's class (Pclass).

Dropped Unnecessary Columns: Removed Cabin (too many missing values), Ticket, and Name as they do not provide predictive value.

Encoded Categorical Features: Converted Sex and Embarked columns into numerical format using one-hot encoding.

Model Training:

The data was split into an 80% training set and a 20% testing set.

A LogisticRegression model from scikit-learn was instantiated and trained on the preprocessed training data.

📊 Results
The model's performance was evaluated on the unseen test set, yielding the following results:

Overall Accuracy: 82%

Classification Report
Class

Precision

Recall

F1-Score

Support

0 (Did not Survive)

0.83

0.87

0.85

105

1 (Survived)

0.80

0.74

0.77

74

Confusion Matrix
The model correctly identified 91 non-survivors and 55 survivors in the test set.

              Predicted
             | 0  | 1  |
-------------------------
Actual   | 0 | 91 | 14 |
         | 1 | 19 | 55 |
-------------------------

🚀 Potential Improvements
The current model serves as a strong baseline. Future work could include:

Feature Engineering: Creating new features like FamilySize (from SibSp + Parch) or IsAlone.

Advanced Imputation: Using more sophisticated techniques (e.g., KNN imputer) for missing Age values.

Alternative Models: Experimenting with more complex algorithms like Random Forest, Gradient Boosting, or Support Vector Machines to potentially improve accuracy.

▶️ How to Run
Clone the repository:

git clone <repository-url>

Install dependencies:

pip install -r requirements.txt

(Note: You may need to create a requirements.txt file or install the libraries listed below manually.)

Execute the script:

python titanic_survival.py

📦 Dependencies
pandas

numpy

matplotlib

seaborn

scikit-learn
