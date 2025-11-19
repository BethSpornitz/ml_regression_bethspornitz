# Final Project – Medical Insurance Cost Regression  
**Author:** Beth Spornitz  
**Date:** November 18, 2025  

---

## Overview  
This repository contains my final machine learning regression project.

The goal of this project is to build and evaluate models that predict medical insurance charges using demographic and lifestyle features. The workflow includes:

- Data exploration  
- Feature engineering  
- Linear Regression  
- Scaled & Polynomial Pipelines  
- Model comparison  
- Final insights & reflections  

---

## Dataset Information

| Field | Description |
|-------|-------------|
| **Dataset Name** | Medical Insurance Dataset |
| **Source** | Kaggle |
| **File** | `data/insurance.csv` |
| **Target Variable** | `charges` (continuous) |

---

## 🔗 Project Files

| File Type | Link |
|-----------|-------|
| 📓 Notebook | **[Regression Notebook – Insurance Charges]([notebooks/regression_final/regression_bethspornitz.ipynb](https://github.com/BethSpornitz/ml_regression_bethspornitz/blob/main/notebooks/regression_final/ml_regression_final_bethspornitz.ipynb))** |
| 📝 Peer Review | **[Peer Review Submission](peer_review.md)** |

---

## 🛠 Workflow 1 – Set Up Machine

Make sure the following tools are installed:

- VS Code  
- Python 3.12  
- uv  
- Git  
- VS Code Extensions: Python, Jupyter, Ruff, Pylance  

---

## 🛠 Workflow 2 – Set Up Project

### 2.1 Clone the Repository

```bash
git clone https://github.com/BethSpornitz/ml_regression_bethspornitz
```

### 2.2 Create and Activate Virtual Environment

```bash
uv venv
uv python pin 3.12
uv sync --extra dev --extra docs --upgrade
uv run pre-commit install
uv run python --version
```

Activate:

```bash
.\.venv\Scripts\activate   # Windows
# or
source .venv/bin/activate # macOS/Linux
```

---

## 🛠 Workflow 3 – Daily Workflow

```bash
git pull
uv sync --extra dev --extra docs --upgrade
uvx ruff check --fix
uv run pre-commit run --all-files
git add .
git commit -m "Update regression project"
```

---

## 🛠 Workflow 4 – Save and Push Work

```bash
git add .
git commit -m "Final regression update"
git push -u origin main
```

---

# Project – Predicting Medical Insurance Charges

This project walks through the complete regression workflow:

### 🔬 Key Steps
| Section | Description |
|---------|-------------|
| **1** | Import & Inspect Data |
| **2** | Data Exploration, Cleaning & Feature Engineering |
| **3** | Feature Selection & Justification |
| **4** | Baseline Linear Regression |
| **5** | Scaled Pipeline & Polynomial Pipeline |
| **6** | Final Thoughts & Reflection |

---

## Model Performance Summary

### Baseline Linear Regression
| Metric | Value |
|--------|--------|
| Train R² | 0.750 |
| Test R² | 0.787 |
| Test MAE | ~$4,204 |
| Test RMSE | ~$5,745 |

### Pipeline 1 – Scaled Linear Regression  
*Identical to baseline (as expected)*

### Pipeline 2 – Polynomial (Degree 3)
| Metric | Value |
|--------|--------|
| Train R² | 0.883 |
| Test R² | 0.860 |
| Test MAE | ~$2,758 |
| Test RMSE | ~$4,662 |

### Key Insight
✔ **Polynomial Regression performed best**  
✔ Captured nonlinear patterns in age, BMI, and smoking  
✔ Scaling alone did not impact performance  
✔ Mild overfitting but strong generalization  

---

### How to Use the Interactive What-If Cost Predictor

- Create and activate the virtual environment as described above.
- Open `regression_final_bethspornitz.ipynb` in VS Code or Jupyter Lab.
- Run all cells.
- Scroll to the section **"Bonus: Interactive What-If Cost Predictor"**.
- Use the sliders (Age, BMI, Children, Smoker, Region) to see the predicted cost update in real time.

---

## 🧪 Engineered Features Used
- `bmi_over_30` (obesity indicator)  
- `age_squared` (nonlinear age effects)  
- `age_bmi_interaction`  
- `smoker_bmi_interaction`  
- `smoker_age_interaction`  
- `has_children`  

---

## 📁 Repository Structure

| File | Purpose |
|------|---------|
| `notebooks/regression_final/regression_bethspornitz.ipynb` 
| `notebooks/data/insurance.csv` 
| `notebooks/peer_review.md` 
| `README.md` 



---
## 🧾 Acknowledgements  
- Instructor: **Dr. Denise Case**  
- Dataset Source: **Kaggle – Insurance Dataset**  
- Tools Used: Python, uv, pandas, scikit-learn, Jupyter, VS Code, Git  
