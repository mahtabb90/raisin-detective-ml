# raisin-detective-ml
Supervised Machine Learning project using Decision Tree, Random Forest and XGBoost to classify raisin types.
# Raisin Detective – Machine Learning Classification Project

## Overview

**Raisin Detective** is a supervised machine learning project where we classify two types of raisins: **Kecimen** and **Besni**.

The project is based on numerical measurements of raisin shape and size, such as area, perimeter, axis lengths and eccentricity. The goal is to investigate whether machine learning models can learn patterns in these measurements and correctly classify the raisin type.

This project was created as part of our Machine Learning course, with focus on:

- Exploratory Data Analysis (EDA)
- Supervised Machine Learning
- Decision Tree
- Random Forest
- XGBoost
- Hyperparameter tuning
- Model evaluation
- Feature Importance
- Permutation Importance
- Data storytelling and business value

---

## Team

This project was developed by:

- Emmy
- Mahtab
- Spirit

---

## Project Story

Imagine a food production company that needs to sort two different raisin types: **Kecimen** and **Besni**.

Manual sorting can be slow, repetitive and sometimes inconsistent. By using machine learning, the company can build a model that automatically classifies raisins based on measurable physical properties.

In this project, our model acts like a small **Raisin Detective**. It looks at each raisin’s size, shape and outer boundary to decide which class it belongs to.

---

## Dataset

The dataset contains **900 raisin samples** and **8 columns**.

There are **7 numerical features** and **1 target variable**.

### Features

- `Area`
- `MajorAxisLength`
- `MinorAxisLength`
- `Eccentricity`
- `ConvexArea`
- `Extent`
- `Perimeter`

### Target

- `Class`

The target contains two classes:

- `Kecimen`
- `Besni`

The dataset is perfectly balanced:

| Class | Count |
|---|---:|
| Kecimen | 450 |
| Besni | 450 |

This makes the dataset suitable for supervised classification.

---

## Machine Learning Workflow

The project follows a complete supervised machine learning workflow:

1. Load and inspect the dataset
2. Perform EDA
3. Check missing values and class balance
4. Analyze relationships between variables
5. Split data into training and test sets
6. Train baseline Decision Tree model
7. Train Random Forest model
8. Tune Random Forest with GridSearchCV
9. Train XGBoost model
10. Compare model performance
11. Analyze Feature Importance and Permutation Importance
12. Summarize results as a data story

---

## Models Used

The following models were tested:

| Model | Accuracy |
|---|---:|
| Decision Tree | 0.844 |
| Random Forest Baseline | 0.867 |
| Tuned Random Forest | 0.872 |
| XGBoost Baseline | 0.856 |
| Tuned XGBoost | 0.850 |

The best model was:

> **Tuned Random Forest**, with approximately **87.2% accuracy**.

---

## Key Insights

The EDA showed that several size-related features are strongly correlated, especially:

- `Area`
- `ConvexArea`
- `Perimeter`
- `MajorAxisLength`

The Feature Importance analysis showed that the most important features were mainly related to size and shape.

The most reliable feature according to Permutation Importance was:

> **Perimeter**

This means that the outer boundary and general shape of the raisin were especially important for classification.

---

## Business Value

This type of machine learning model could be useful in food production and quality control.

A company could use a similar model to:

- Automate product sorting
- Reduce manual work
- Improve consistency
- Reduce human error
- Support quality control
- Save time in production

Even though this is a small educational project, it demonstrates how supervised machine learning can support decision-making in real-world production environments.

---

## Project Structure

```text
raisin-detective-ml/
│
├── data/
│   └── raw/
│       ├── Raisin_Dataset.xlsx
│       └── raisin_dataset.csv
│
├── notebooks/
│   ├── emmy/
│   ├── mahtab/
│   │   ├── 01_data_loading_and_eda.ipynb
│   │   ├── 02_preprocessing_and_baseline_models.ipynb
│   │   ├── 03_random_forest_model.ipynb
│   │   ├── 04_feature_importance_and_permutation.ipynb
│   │   ├── 05_xgboost_model.ipynb
│   │   └── 06_final_summary_and_story.ipynb
│   └── spirit/
│
├── reports/
│
├── requirements.txt
├── README.md
└── .gitignore

