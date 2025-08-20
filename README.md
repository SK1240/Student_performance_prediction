# 🎓 Student Performance Prediction System
## 📌 Project Snapshot
A machine learning system that predicts a student’s math score (academic performance) using regression models.

🔍 The system analyzes multiple factors:
* 👤 Gender 
* 🧑‍🤝‍🧑 Ethnicity 
* 🎓 Parental Education 
* 🍴 Lunch Type
* 📘 Reading 
* ✍️ Writing 
* 📚 Prep Course

The goal is to build a robust regression pipeline that can generalize well and provide accurate predictions of a student's math score (or overall academic performance).

The project includes: ✅ **Multiple regression algorithms** (Linear Regression, Ridge, Lasso, Random Forest, Gradient Boosting, XGBoost, etc.) ✅ **ML Pipelines** for preprocessing + modeling ✅ **Flask web application** for user interaction ✅ **Dockerized Deployment** for Run anywhere with a single container.

## 📊 Example Prediction

| gender	|  race/ethnicity | parental level	|   lunch	   | prep course	|   reading score   | 	writing score   |
|---------|-----------------|-----------------|------------|--------------|-------------------|-------------------|
|  female	|      group B	  |   bachelor's	  |  standard	 |  completed	  |        72	        |          74       |

**➡️ Predicted Math Score: 🎯 78.5**

## 🚀 Key Features

* ✨ End-to-end ML pipeline: Ingestion → Preprocessing → Training → Prediction
* 📊 Comparative analysis of multiple regression models
* ⚙️ Hyperparameter tuning for optimization
* 🌐 Flask Web App for real-time predictions
* 🐳 Dockerized deployment (runs anywhere)


## 🛠️ Tech Stack

* 🖥️ Python 3.11+
* 🌐 Flask – Web Framework
* 📚 Scikit-learn, XGBoost, CatBoost – ML & Preprocessing
* 📦 Dill – Model Serialization
* 🐳 Docker – Containerization
* ☁️ AWS CLI – Cloud Integration
