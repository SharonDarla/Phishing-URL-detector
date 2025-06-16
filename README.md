# Phishing-URL-detector 

Phishing URL Detection Using Machine Learning: This project implements and compares various machine learning models to detect phishing URLs based on features extracted from domain names and URLs. The goal is to classify domains as either benign or phishing using techniques such as Random Forest , Gradient Boosting , a Neural Network , and an ensemble model that combines predictions from all three.

# Project Overview

The project performs the following steps:

Loads and preprocesses URL/domain data.
Trains multiple classifiers with hyperparameter tuning.
Evaluates individual models using cross-validation and feature importance analysis.
Builds a neural network classifier.
Combines predictions from all models into an ensemble method.
Visualizes performance metrics (confusion matrix, ROC curve, Precision-Recall curve).

# Requirements

To run this project, ensure you have Python installed along with the following libraries:
pip install pandas numpy scikit-learn matplotlib seaborn tensorflow
pip install plotly

# Dataset
The dataset was named as combined_dataset.csv.
It contains:
A column named 'label' indicating whether a domain is phishing (1) or benign (0).
A column named 'domain' which will be excluded during training.
Other columns are treated as features for classification (e.g., length, entropy, SSL info, etc.).

# Project Structure

| Stages | Description |
| Data Loading | Reads the CSV file and displays the first few rows. |
|:-----------:|:------------------------------:|
|Preprocessing | Drops irrelevant columns, scales features, and splits into train/test sets.|
|:----------:|:-----------------|
| Model Training | Trains Random Forest, Gradient Boosting, and Neural Network models with hyperparameter tuning. |
|:-------------------:|:-------------------:|
| Cross-Validation | Evaluates Random Forest and Gradient Boosting using K-Fold Cross Validation. |
Feature Importance
Plots the most influential features for each tree-based model.
Ensemble Model
Combines predictions from all three models using probability averaging.
Evaluation
Reports accuracy, confusion matrix, classification report, ROC curve, and Precision-Recall curve.
