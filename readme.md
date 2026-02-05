# 🎗️ Breast Cancer Prediction using K-Nearest Neighbors (KNN)

## 📌 Project Overview
This project applies the **K-Nearest Neighbors (KNN)** algorithm to predict whether a breast tumor is **benign or malignant** using the **Breast Cancer Wisconsin dataset**.

The goal is to build a reliable classification model by:
- Cleaning missing data
- Selecting optimal `k` value
- Evaluating model accuracy
- Making predictions on new patient records

---

## 📊 Dataset Description
- Dataset: Breast Cancer Wisconsin (Original)
- Total samples (after cleaning): **683**
- Target variable: `class`
  - `2` → Benign
  - `4` → Malignant

### Features Used
- Clump Thickness
- Uniformity of Cell Size
- Uniformity of Cell Shape
- Marginal Adhesion
- Single Epithelial Cell Size
- Bare Nuclei
- Bland Chromatin
- Normal Nucleoli
- Mitoses

---

## 🧹 Data Cleaning & Preprocessing
- Removed rows containing missing values (`?`) in `bare_nulei`
- Dropped non-informative `id` column
- Ensured all features were numeric
- Split data into **80% training** and **20% testing**

---

## 🛠️ Tools & Libraries Used
- Python
- Pandas
- Matplotlib
- Scikit-learn

---

## 🤖 Model Building
- **Algorithm:** K-Nearest Neighbors (KNN)
- Distance Metric: Euclidean (default)
- Initial `k` value estimated using:  
  `k = √(number of test samples)`
- Final optimal `k` selected using accuracy comparison

---

## 📈 Model Performance

### Initial K (k = 11)
- **Accuracy:** **95.62%**

### Accuracy for Different k Values
| k | Accuracy |
|---|---------|
| 1 | 97.81% |
| 3 | **97.08%** |
| 5 | 97.08% |
| 7 | 97.08% |
| 11 | 95.62% |

📌 **Final Model:** `k = 3`

- **Final Accuracy:** **97.08%**

---

## 🔮 Predictions

### Example 1
```python
model.predict([[4, 2, 1, 1, 1, 2, 3, 2, 1]])
Prediction: 2 → Benign

