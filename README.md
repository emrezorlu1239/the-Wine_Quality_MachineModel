# 🍷 the-Wine_Quality_MachineModel

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)
![Random Forest](https://img.shields.io/badge/Model-Random%20Forest-success.svg)
![Accuracy](https://img.shields.io/badge/Accuracy-90.2%25-green.svg)

**the-Wine_Quality_MachineModel** is an end-to-end machine learning project designed to predict wine quality classes by analyzing physicochemical properties. By utilizing raw data through feature engineering and imbalanced class management strategies, the model achieved an accuracy rate of **90.20%**.

---

## 🎯 Project Objective
This study aims to automate quality control processes in wine production and quantitatively measure the impact of chemical components on the final quality score. The model is optimized to distinguish "Premium" (7+ score) wines from "Standard" (<=6 score) wines with the highest precision.



---

## 🛠️ Data Science Pipeline

### 1. Data Preprocessing
* **Target Transformation:** Quality scores ranging from 3 to 9 were converted into a binary class:
    * **Class 0 (Standard):** Quality Score $\le 6$
    * **Class 1 (Premium):** Quality Score $\ge 7$
* **Scaling:** `StandardScaler` was applied to eliminate magnitude differences between variables and ensure model stability.

### 2. Feature Engineering
Two new metrics were engineered to better capture the balance and body of the wine:
* **Acid-Alcohol Ratio:** Represents the balance between freshness and strength.
* **Sulphate-Density Ratio:** Represents the distribution of preservatives relative to the wine's density.

### 3. Model Architecture: Random Forest Classifier
Random Forest was selected for its ability to capture non-linear relationships and its inherent resistance to overfitting.
* **Class Weighting:** To ensure the minority "Premium" class is not overlooked, the `class_weight={0: 1, 1: 5}` parameter was used, increasing the model's sensitivity to Premium samples fivefold.

---

## 📊 Performance Analysis

The model's performance was validated using both standard test data and a "Blind Test" simulation consisting of extreme scenarios.

### Test Set Metrics:
| Metric | Score |
| :--- | :--- |
| **Overall Accuracy** | **90.20%** |
| **Standard Wine Recall** | **98%** |
| **Premium Wine Precision** | **77%** |



### Blind Test Simulation
The model demonstrated strong generalization capabilities by achieving over **80%** success on a 20-sample synthetic profile set, proving its robustness against real-world data variations.

---

## 🚀 Installation and Usage

1. **Clone the Repo:**
   ```bash
   git clone [https://github.com/](https://github.com/)[Your-Username]/the-Wine_Quality_MachineModel.git
   cd the-Wine_Quality_MachineModel
