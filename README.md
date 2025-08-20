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

## 📂 Project Structure

```bash
📦 Student-Performance/
├── .gitignore
├── application.py          # Flask entry point
├── Dockerfile              # Docker container setup
├── requirements.txt        # python Dependencies
├── setup.py                # Package setup
├── notebook/               # jupyter Notebooks & dataset
│   ├── data/StudentsPerformance.csv
│   ├── 1_EDA.ipynb
│   └── 2_Model_Training.ipynb
├── templates/              # HTML templates
│   ├── index.html
│   └── home.html
├── Source/                 # Core ML pipeline
│   ├── Components/
│   │   ├── data_ingestion.py          # Data ingestion & train/test split
│   │   ├── data_transformation.py     # Preprocessing pipelines
│   │   └── model_trainer.py           # Model training & evaluation
│   ├── pipeline/
│   │   ├── predict_pipeline.py        # Inference pipeline for predictions
│   │   └── train_pipeline.py          # Inference pipeline for training
│   ├── exception.py                   # Custom exception handling 
│   ├── logger.py                      # Logging utility
│   └── utils.py                       # Helper functions (save/load/eval)
├── artifacts/              # Trained model & preprocessor
│   ├── model.pkl                      # Trained ML model
│   └── preprocessor.pkl               
├── logs/                   # Log files
```


## ⚙️ Setup & Installation

### 1️⃣. Clone the Repository

```
git clone https://github.com/SK1240/Student_performance_prediction
cd Student-Performance
```

### 2️⃣ Create Virtual Environment

```
python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows
```

### 3️⃣ Install Dependencies

```
pip install -r requirements.txt
```

### 4️⃣ Run Flask App

```
python application.py
```

### 🌍 Access App:

🏠To Check Home: 👉 [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

🎯To Check Predict: 👉 [http://127.0.0.1:5000/predictdata](http://127.0.0.1:5000/predictdata)


## 🔄 Pipeline Workflow

1. **Data Ingestion** (`data_ingestion.py`)

    • Reads raw dataset (`StudentsPerformance.csv`).                      
    • Splits into train/test datasets.                    
    • Stores CSVs in `artifacts/`.   

2. **Data Transformation** (`data_transformation.py`)

    • Handles missing values with `SimpleImputer`.                      
    • Scales numerical columns (`StandardScaler`).                         
    • Encodes categorical features (`OneHotEncoder`).                        
    • Saves preprocessing pipeline as `preprocessor.pkl`. 

3. **Model Training** (`model_trainer.py`)

    • Trains multiple regression algorithms.                      
    • Uses **GridSearchCV/RandomizedSearchCV** for hyperparameter tuning.                               
    • Selects best model and saves as `model.pkl`.  

4. **Prediction Pipeline** (`prediction_pipeline.py`)

    • Loads trained model + preprocessor.                      
    • Accepts user input, preprocesses, and predicts math score.  

5. **Flask Application** (`application.py`)

    • Web form to input features.                                  
    • Displays prediction results. 

6. **Custom Utilities**

    • `exception.py`: Custom structured exception handling.                    
    • `logger.py`: Timestamped logging with rotating logs.                
    • `utils.py`: Save/load objects, evaluate models. 


## 🔮 Future Enhancements