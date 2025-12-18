Predicting News Engagement Under Context Drift
Evan McLaughlin – CUNY MS Data Science Capstone
Overview

This repository contains the code used for my capstone project examining news engagement prediction under context drift. The analysis compares metadata- and text-based models across two datasets with fundamentally different engagement mechanisms:
UCI Online News Popularity (Mashable, ~2014)
Target: social shares
Microsoft MIND-small (News recommendation, ~2019)
Target: click-through behavior
The project emphasizes interpretability, model failure analysis, and context sensitivity, rather than pure predictive performance.

Key Components of the Notebook
-Data Ingestion and Preprocessing
-Handles headerless MIND data files
-Cleans and aligns impressions and news metadata
-Constructs modeling datasets for UCI and MIND
-Exploratory Data Analysis
-Engagement distribution analysis
-Metadata feature inspection
-Class imbalance diagnostics (MIND)
-Baseline Modeling
-Linear regression (UCI metadata)
-Gradient boosting (UCI metadata)
-TF-IDF + logistic regression baseline (MIND)
-Model Evaluation
-RMSE, MAE, R² for regression tasks
-Precision, recall, F1 for classification
-Explicit discussion of misleading accuracy under class imbalance
-Interpretability and Stability
-SHAP value analysis for tree-based models
-Stability checks across random splits
-Cross-dataset SHAP comparison to visualize context drift
-LLM-Derived Virality Feature (MIND only)
-Uses an OpenAI API call to generate a scalar “virality score”
-Encodes narrative framing, emotional appeal, and novelty
-Designed to bridge human editorial judgment and machine learning features
