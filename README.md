# MACHINE-LEARNING-INSURANCE-COST-PREDICTION-
Here’s a polished **README.md** for your GitHub portfolio project, including your dataset source, evaluation metrics, and all the details you provided.

---

# 🏥 Insurance Cost Prediction – Machine Learning Project

## 📌 Overview

This project focuses on building a **Machine Learning model** to predict **medical insurance costs** using demographic and lifestyle features from a publicly available dataset. The goal is to identify the most accurate model for this regression task and provide an easy-to-use **GUI application** for making predictions.

**Target Variable:** `charges` – the predicted insurance cost in USD.

**Dataset Source:** [Kaggle – Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)

---

## 📊 Features Used

* **Age** – Age of the individual (in years)
* **Sex** – Male / Female
* **BMI** – Body Mass Index (kg/m²)
* **Children** – Number of children/dependents covered by insurance
* **Smoker** – Yes / No
* **Region** – U.S. region (northeast, northwest, southeast, southwest)

---

## 🧠 Algorithms Tested

1. **Linear Regression**
2. **Random Forest Regressor**
3. **Support Vector Machine (SVM)**
4. **Gradient Boosting Regressor** ✅ *(Best performer)*

We trained all four models, evaluated them using **Root Mean Squared Error (RMSE)** and **Mean Absolute Error (MAE)**, and selected the best-performing model for deployment.

---

## 📈 Model Performance

| Algorithm               | RMSE       | MAE               |
| ----------------------- | ---------- | ----------------- |
| Linear Regression       | 0.7833     | 33,635,210.43     |
| Random Forest Regressor | 0.8636     | 21,163,477.29     |
| Support Vector Machine  | -0.0723    | 166,472,846.51    |
| **Gradient Boosting** ✅ | **0.8780** | **18,941,336.01** |

---

## 💾 Saving & Loading the Model

We used **Joblib** to store and retrieve the trained model.

```python
from joblib import dump, load

# Save model
dump(best_model, 'best_model.joblib')

# Load model
model = load('best_model.joblib')
```

---

## 🖥 GUI Application

At the end of the project, we developed a **Tkinter-based GUI** that allows users to input custom values for each feature and instantly receive the predicted insurance cost.

### Running the GUI

```bash
python gui/insurance_gui.py
```

---

## 📂 Project Structure

```
insurance-cost-prediction/
│
├── data/
│   └── insurance.csv
│
├── notebooks/
│   └── EDA_and_Model_Training.ipynb
│
├── models/
│   └── best_model.joblib
│
├── gui/
│   └── insurance_gui.py
│
├── README.md
└── requirements.txt
```

---

