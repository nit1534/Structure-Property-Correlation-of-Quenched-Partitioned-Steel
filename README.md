# 🔩 QP Steel Strength Prediction

A machine learning project to predict the **Yield Strength (YS)** and **Ultimate Tensile Strength (UTS)** of Quenching & Partitioning (Q&P) steels using chemical composition data.

---

## 📌 Overview

This project uses an ensemble of **XGBoost**, **Random Forest**, and **ANN (Artificial Neural Network)** models to predict mechanical properties of steel based on its chemical composition. The model is trained and evaluated using 5-fold cross-validation and holdout testing.

---

## 📁 Project Structure

```
steel-project/
├── ann_model.py                # Main model training and plotting script
├── hardwork_adjusted.xlsx      # Input dataset (chemical composition + strength values)
├── qp_steel_results.png        # Output plot (auto-generated after running)
└── README.md                   # Project documentation
```

---

## 🧪 Input Features (Chemical Composition)

| Feature | Description |
|--------|-------------|
| C | Carbon |
| Si | Silicon |
| Mn | Manganese |
| Cr | Chromium |
| Al | Aluminium |
| Ni | Nickel |
| P | Phosphorus |
| S | Sulphur |
| Ti | Titanium |
| V | Vanadium |

---

## 🎯 Target Variables

- **YS (MPa)** — Yield Strength
- **UTS (MPa)** — Ultimate Tensile Strength

---

## 🤖 Models Used

| Model | Description |
|-------|-------------|
| XGBoost | Gradient boosting with 600 estimators |
| Random Forest | Ensemble of 400 decision trees |
| ANN | Multi-layer perceptron (128 → 64 → 32 neurons) |
| Ensemble | Weighted average: 55% XGBoost + 45% Random Forest |

---

## 📊 Output Plots

After running the script, `qp_steel_results.png` is generated containing:
- Parity plots (Actual vs Predicted) for YS and UTS
- 5-fold Cross-Validation R² comparison
- Residual plots
- Feature importance charts (XGBoost permutation)

---

## ⚙️ How to Run

### 1. Install dependencies
```bash
pip install pandas numpy matplotlib scikit-learn xgboost seaborn openpyxl
```

### 2. Place your dataset
Make sure `hardwork_adjusted.xlsx` is in the **same folder** as `ann_model.py`.

### 3. Run the script
```bash
python ann_model.py
```

---

## 📦 Requirements

- Python 3.8+
- pandas
- numpy
- matplotlib
- scikit-learn
- xgboost
- seaborn
- openpyxl

---

## 📈 Results

The ensemble model (XGBoost + Random Forest) achieves strong predictive performance:
- High R² scores on both YS and UTS
- Low RMSE and MAE on holdout test set
- Robust 5-fold cross-validation results

---
