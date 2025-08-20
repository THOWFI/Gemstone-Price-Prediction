# 💎 Gemstone Price Prediction

An advanced **end-to-end Machine Learning project** that predicts gemstone prices based on their attributes.  
This repository implements a **modular ML pipeline** with Flask integration for real-time predictions and production-ready deployment.

---

## 📌 Project Overview

Gemstone valuation depends on several measurable attributes such as:

- **Carat** (weight of the gemstone)  
- **Cut** (quality of cut: Fair, Good, Very Good, Premium, Ideal)  
- **Color** (graded from D–J)  
- **Clarity** (from I1 to IF)  
- **Depth & Table** proportions  
- **Other measurable features**

This project leverages **machine learning regression algorithms** to automate and improve gemstone price estimation.  

The system includes:
✅ Multiple regression algorithms (Linear Regression, Random Forest, XGBoost, CatBoost, etc.)  
✅ **Modular ML pipelines** for ingestion, preprocessing, and training  
✅ **Flask Web Application** for real-time predictions  
✅ **Logging & Exception handling** for reliability  
✅ **Deployment-ready** with setup scripts  

---

## 📊 Example

| Carat | Cut     | Color | Clarity | Depth | Table |
|-------|---------|-------|---------|-------|-------|
| 1.2   | Premium | E     | VS1     | 61.5  | 57    |

✅ Output → Predicted Gemstone Price: **5,820**

---

## 🚀 Features

- End-to-end **ML pipeline** (data ingestion → transformation → training → evaluation → prediction).  
- Comparative analysis of multiple regression models.  
- Hyperparameter tuning for optimized performance.  
- **Flask-based web interface** for user interaction.  
- **Artifacts management** (stores preprocessed data, trained models, logs).  
- Modular and extensible codebase for research or production.  

---

## 🛠️ Tech Stack

- **Python 3.11+**  
- **Flask** – Web framework  
- **Scikit-learn** – Preprocessing, training & evaluation  
- **XGBoost / CatBoost** – Advanced regression models  
- **Pandas & NumPy** – Data handling  
- **Matplotlib / Seaborn** – Visualization (EDA)  
- **Dill / Pickle** – Model serialization  

---

## 📂 Project Structure

```bash
Gemstone-Price-Prediction/
│── application.py              # Flask app entry point
│── requirements.txt            # Python dependencies
│── setup.py                    # Package setup
│── .gitignore
│── README.md                   # Project documentation
│
├── artifacts/                  # Generated artifacts
│   ├── data.csv
│   ├── train.csv
│   ├── test.csv
│   ├── model.pkl
│   └── preprocessor.pkl
│
├── logs/                       # Log files
│
├── notebook/                   # Jupyter notebooks
│   ├── data/gemstone.csv       # Raw dataset
│   ├── 1_EDA_Gemstone_price.ipynb
│   └── 2_Model_Training_Gemstone.ipynb
│
├── src/                        # Core ML source code
│   ├── components/             # ML pipeline components
│   │   ├── data_ingestion.py   # Loads dataset & splits train/test
│   │   ├── data_transformation.py # Preprocessing & feature engineering
│   │   └── model_trainer.py    # Model training & evaluation
│   │
│   ├── pipeline/
│   │   ├── train_pipeline.py   # High-level training pipeline
│   │   └── predict_pipeline.py # Final prediction pipeline
│   │
│   ├── exception.py            # Custom exception handling
│   ├── logger.py               # Logging utility
│   └── utils.py                # Helper functions (save/load models)
│
├── templates/                  # Flask HTML templates
│   └── index.html
│
└── static/css/                 # CSS for UI
    └── style.css
```

## 🧩 Pipeline Workflow

1. **Data Ingestion** (```bash data_ingestion.py```)         
- Reads dataset (```bash gemstone.csv```)          
- Splits into train/test sets               
- Stores CSVs in artifacts/             

2. **Data Transformation** (```bash data_transformation.py```)
- Handles missing values
- Encodes categorical variables (cut, color, clarity)
- Scales numerical features (carat, depth, table, etc.)
- Saves preprocessing object as preprocessor.pkl

3. **Model Training** (```bash model_trainer.py```)
- Trains multiple regression models
- Uses GridSearchCV/RandomizedSearchCV for hyperparameter tuning
- Saves best model as model.pkl

4. **Training Pipeline** (```bash train_pipeline.py```)
- Orchestrates full pipeline (ingestion → transformation → training)

5. **Prediction Pipeline** (```bash predict_pipeline.py```)
- Loads model.pkl & preprocessor.pkl
- Accepts user input → preprocess → predict gemstone price

6. **Flask Application** (```bash application.py```)
- Web form for user input
- Displays predicted gemstone price in real-time

7. **Utilities**
- ```bash logger.py``` : Structured logging
- ```bash exception.py``` : Custom error handling
- ```bash utils.py``` : Model saving/loading, evaluation functions

---

## ⚙️ Installation & Setup

## 1️⃣ Clone Repository
    git clone https://github.com/THOWFI/Gemstone-Price-Prediction.git
    cd Gemstone-Price-Prediction

## 2️⃣ Create Virtual Environment
    python -m venv venv
    source venv/bin/activate   # Linux/Mac
    venv\Scripts\activate      # Windows

## 3️⃣ Install Dependencies
    pip install -r requirements.txt

## 4️⃣ Run Flask App
    python application.py

---

**Visit :**
👉 http://127.0.0.1:8000/

👉 http://127.0.0.1:8000/predictdata

---

## 📊 Results
- Best model: Random Forest / XGBoost / CatBoost (dataset-dependent)
- Metrics achieved:
    - R² Score: ~0.93+
    - RMSE: Low prediction variance
    - MAE: Small error in gemstone price predictions

---

## 🔮 Future Enhancements
- 📊 Model Explainability → SHAP/LIME feature importance
- ☁️ Full AWS Deployment → Elastic Beanstalk / S3 / Lambda integration
- 📱 UI Upgrade → Streamlit or React-based dashboard
- 🔄 Continuous Training → Auto retrain with new gemstone data

  
---

## 📜 License
This project is not licensed for public use.

