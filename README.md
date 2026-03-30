# E-commerce Customer Intelligence Framework

**Personalized Product Recommendations + Customer Churn Prediction**

An end-to-end machine learning solution that combines **hybrid recommendation systems** with **predictive churn analytics** to drive customer engagement and retention for e-commerce platforms.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## 📋 Project Overview

This project develops a unified **E-commerce Customer Intelligence Framework** using the Retailrocket dataset. It addresses two critical business challenges:

- **Growth Engine**: Delivering personalized product recommendations to increase engagement and sales.
- **Retention Engine**: Predicting customer churn to enable proactive intervention and protect customer lifetime value.

By integrating both systems, the framework supports intelligent customer lifecycle management — from discovery to long-term loyalty.

### Key Objectives
- Build a **hybrid recommendation system** (Collaborative Filtering + Content-Based)
- Develop an **interpretable churn prediction model** using RFM and behavioral features
- Provide **actionable business insights** and retention strategies
- Deliver a clean, reproducible, and well-documented pipeline

---

## 🗂️ Dataset

**Retailrocket E-commerce Dataset**  
[Download from Kaggle](https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset/data)

### Files Used:
- `events.csv` — 2.75M+ user interactions (view, addtocart, transaction)
- `item_properties_part1.csv` & `item_properties_part2.csv` — Time-dependent product attributes (~417K items)
- `category_tree.csv` — Hierarchical category structure

**Note**: Due to large file sizes, this repository contains **sampled versions** (`events_sample.csv`, etc.) for demonstration.  
Full dataset can be downloaded from the Kaggle link above.

---

## ✨ Features & Approach

### 1. Recommendation Engine
- **Hybrid Model**: SVD-based Collaborative Filtering + Category-based Content Filtering
- **Weighting**: 70% collaborative + 30% content (`alpha = 0.7`)
- **Cold-start Handling**: Automatic fallback to popularity-based recommendations for new users
- **Evaluation Metrics**: Precision@10, Recall@10, NDCG@10

### 2. Customer Churn Prediction
- **Feature Engineering**: RFM metrics, behavioral ratios, recency flags, high-value segments
- **Model**: Logistic Regression (chosen for interpretability and business explainability)
- **Threshold Optimization**: F1-optimal threshold for balanced precision and recall
- **Evaluation**: ROC-AUC, Classification Report, Feature Importance (Odds Ratios)

### 3. Business Translation
- Clear churn drivers interpretation (Recency is the strongest predictor)
- Actionable retention strategies based on churn probability and user segments

---

## 📊 Results Highlights

- **Churn Model**: Strong performance with clear business insights — recency and purchase behavior are key drivers.
- **Recommendation System**: Hybrid approach significantly outperforms pure popularity baseline.
- **Interpretability**: Logistic Regression coefficients translated into actionable odds ratios.
- **Business Value**: Ready-to-use retention rules (e.g., trigger personalized offers when churn probability > 0.65).

---

## 🛠️ Tech Stack

- **Language**: Python 3.12
- **Data Processing**: pandas, numpy
- **Modeling**: scikit-learn, implicit (for SVD)
- **Visualization**: matplotlib, seaborn
- **Environment**: Jupyter Notebook

---

## 📁 Project Structure
