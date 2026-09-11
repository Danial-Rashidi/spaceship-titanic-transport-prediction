# 🚀 Spaceship Titanic — Passenger Transport Prediction

A machine learning classification project developed for the **Spaceship Titanic** Kaggle competition.

The goal is to predict whether a passenger was transported to another dimension after the Spaceship Titanic anomaly.

This project explores the full modeling process, from initial preprocessing and baseline models to feature engineering, ensemble methods, and final CatBoost optimization.

---

## 📊 Dataset

The dataset is provided by the **Kaggle Spaceship Titanic** competition.

The original dataset contains passenger information such as:

- PassengerId
- HomePlanet
- CryoSleep
- Cabin
- Destination
- Age
- VIP
- Spending information
- Transported

The original `train.csv` and `test.csv` files are **not included in this repository**.

You can download the dataset directly from Kaggle:

**https://www.kaggle.com/competitions/spaceship-titanic**

After downloading, place the files next to the notebook:

- train.csv
- test.csv

---

## Note
The repository intentionally contains one integrated notebook rather than every experimental notebook and intermediate file.

During development, several intermediate CSV files were created, including files such as:

- train_clean.csv
- test_clean.csv
- submission1.csv
- submission2.csv
- submission_catboost.csv
- submission_Xgboost.csv
- submission_nn.csv
- submission_knn.csv

---
##🤖 Models

Several different machine learning approaches were tested throughout the project:

Random Forest
CatBoost
XGBoost
Neural Network
K-Nearest Neighbors

The experiments were used to compare different model families and determine which approaches were most effective for this classification problem.

##📈 Model Results

The main Kaggle results obtained during development were:

Model	Kaggle Score
Random Forest baseline	0.79541
Random Forest + Feature Engineering	0.79003
CatBoost	0.80687
XGBoost	0.80079
Neural Network	0.62450
KNN	0.70797

Tree-based gradient boosting models performed substantially better than the Neural Network and KNN approaches.

##🏆 Final Model

CatBoost produced the strongest individual result and was therefore selected for further optimization.

A randomized hyperparameter search was performed across multiple configurations, exploring parameters such as:

Learning rate
Tree depth
L2 regularization
Random strength
Bagging temperature
Border count
Feature sampling

Early stopping was used during validation to select an appropriate number of iterations.

The best configuration was then retrained on the complete training dataset and used to generate the final submission.

#🥇 Final Kaggle Result

Kaggle Score: 0.80757

This was the final submitted result for the competition.
