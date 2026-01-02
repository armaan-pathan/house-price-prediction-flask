# House Price Prediction WebApp 

This project is a **House Price Prediction Web Application** built with **Flask**.
It uses the **USA Housing dataset** and multiple **regression models** to predict housing prices.

Users can enter housing details via a web form, choose an algorithm, and get price predictions instantly. The app also provides a **model comparison table** to evaluate all trained regression models.

---

## Features

* Train multiple regression models on the USA Housing dataset:

  * Linear Regression
  * Ridge Regression (L2)
  * Lasso Regression (L1)
  * ElasticNet Regression
  * Polynomial Regression
  * SGD Regressor
  * Artificial Neural Network (MLP Regressor)
  * Random Forest Regressor
  * Support Vector Regressor
  * LightGBM Regressor
  * XGBoost Regressor
  * KNN Regressor
  * Robust Regression
* Save trained models as `.pkl` files inside a **models/** folder.
* Flask-based frontend for:

  * Entering inputs & selecting an algorithm.
  * Displaying prediction results.
  * Viewing model evaluation metrics (MAE, MSE, R²) in a comparison table.

---

## Project Structure

```
Day48_House_Price_Prediction_Project/
│── Day48_House_Price_Prediction_Project.py   # Training & saving models
│── app.py                                    # Flask app
│── model_evaluation_results.csv              # Evaluation results
│── README.md                                 # Project documentation
│
├── models/                                   # All saved regression models
│   ├── linear_model.pkl
│   ├── ridge_model.pkl
│   ├── lasso_model.pkl
│   ├── elasticnet_model.pkl
│   ├── polynomial_model.pkl
│   ├── randomforest_model.pkl
│   ├── svm_model.pkl
│   ├── xgboost_model.pkl
│   ├── knn_model.pkl
│   └── ...
│
└── templates/                                # Flask frontend
    ├── index.html     # Form for input
    ├── model.html     # Model evaluation table
    └── results.html   # Prediction results
```

---

## Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/armaan-pathan/fsds-genai-2025.git
cd fsds-genai-2025/Projects/Day48_House_Price_Prediction_Project
```

### 2️⃣ Create & activate virtual environment

```bash
python -m venv venv
venv\Scripts\activate   # On Windows
source venv/bin/activate   # On Mac/Linux
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

## How to Run

### Step 1: Train & Save Models

Run the training script to train all regression models and save them in the **models/** folder:

```bash
python Day48_House_Price_Prediction_Project.py
```

This will also generate `model_evaluation_results.csv` with MAE, MSE, and R² scores for each model.

---

### Step 2: Start Flask App

Run the Flask app:

```bash
python app.py
```

By default, the app runs on:

```
http://127.0.0.1:5000/
```

---

### Step 3: Use the WebApp

1. Open the app in your browser.
2. Enter housing details:

   * Avg Area Income
   * Avg Area House Age
   * Avg Area Number of Rooms
   * Avg Area Number of Bedrooms
   * Area Population
3. Select the regression model.
4. Click **Predict** → The predicted price is displayed.
5. Click on **Model Evaluation** to view the comparison table of all trained models.

---

## Model Evaluation

During training, all models are evaluated using:

* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**
* **R² (Coefficient of Determination)**

These results are stored in `model_evaluation_results.csv` and displayed in the webapp (`model.html`).

---

## Takeaways

* Built a **complete ML pipeline** → from preprocessing → training → saving → deployment.
* Learned to integrate **multiple regression models** into a **Flask webapp**.
* Practiced **model evaluation, saving/loading, and frontend integration**.

