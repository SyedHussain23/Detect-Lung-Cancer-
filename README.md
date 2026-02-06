# 🫁 Lung Cancer Survival Prediction using Machine Learning

This project builds an end-to-end **machine learning classification system** to predict **patient survival outcomes** based on medical diagnosis and treatment data.  
It demonstrates a complete beginner-friendly ML workflow including data loading, preprocessing, feature engineering, model training, evaluation, and prediction.

⚠️ **Note:** This project highlights real-world challenges such as **class imbalance**, which significantly impacts model performance.

---

## 📌 Project Overview

- **Problem Type:** Binary Classification  
- **Domain:** Healthcare / Medical Analytics  
- **Goal:** Predict whether a lung cancer patient survived (`1`) or not (`0`)  
- **Model Used:** Random Forest Classifier  
- **Key Challenge:** Highly imbalanced target variable  

---

## 📊 Dataset

- **Source:** Medical diagnosis dataset (`dataset_med.csv`)
- **Records:** ~890,000 patients
- **Target Variable:** `survived` (0 = No, 1 = Yes)
- **Features Include:**
  - Demographics (gender, country)
  - Medical details (cancer stage, family history)
  - Lifestyle factors (smoking status)
  - Treatment type
  - Diagnosis and treatment dates

---

## 🔍 Exploratory Data Analysis (EDA)

Key findings:
- No missing values after preprocessing
- Target variable is **severely imbalanced**
- Majority of patients did **not survive**
- Numerical and categorical features present
- Large dataset suitable for tree-based models

---

## 🔧 Data Preprocessing

Steps performed:
- One-hot encoding for categorical features:
  - gender, country, cancer stage, smoking status, treatment type, etc.
- Converted date columns to datetime
- Created new engineered feature:
  - **`treatment_duration_days`** = end treatment date − diagnosis date
- Dropped original date columns
- Prepared final feature matrix for modeling

---

## 🧠 Feature Engineering

New feature added:
- **Treatment Duration (days)**  
  Helps capture the intensity and length of medical intervention

---

## 🧪 Train–Test Split

- **Training Set:** 75%
- **Testing Set:** 25%
- Ensured reproducibility with `random_state=42`

---

## 🤖 Model Building

### Model Used
- **Random Forest Classifier**

Why Random Forest?
- Handles large datasets well
- Captures non-linear relationships
- Robust to feature scaling
- Suitable baseline for medical tabular data

---

## 📈 Model Evaluation

### Test Set Performance

- **Accuracy:** ~77.88%
- **Precision:** ~15.38%
- **Recall:** ~0.01%
- **F1-score:** ~0.02%

### Interpretation
- High accuracy is **misleading** due to class imbalance
- Model predicts majority class (non-survival) well
- Very poor recall for survival cases
- Demonstrates why accuracy alone is not sufficient in healthcare ML

---

## 🔮 Predictions

- Model generates survival predictions for unseen patient records
- Output:
  - `0` → Did not survive
  - `1` → Survived

Predictions are stored for further analysis or downstream use.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|-----|--------|
| Python | Programming |
| Pandas / NumPy | Data handling |
| Scikit-learn | Machine learning |
| Random Forest | Classification model |
| Jupyter Notebook | Development environment |

---

## 🚀 How to Run

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/SyedHussain23/Detect-Lung-Cancer-.git
cd Detect-Lung-Cancer-
pip install pandas numpy scikit-learn
jupyter notebook Detect Lung Cancer.ipynb
```

---

## ⚠️ Limitations & Learnings

- Dataset is highly imbalanced
- Survival class is underrepresented
- Accuracy alone is not a reliable metric in medical predictions
- Highlights importance of:
  - Recall
  - F1-score
  - Class-aware evaluation
 
---

## 🔮 Future Improvements

- Handle class imbalance using:
   - SMOTE / oversampling
   - Class-weighted models
- Evaluate using ROC-AUC and PR-AUC
- Try Gradient Boosting or XGBoost
- Hyperparameter tuning
- Build a survival risk scoring system
- Add explainability (feature importance / SHAP)

---

👨‍💻 Author

**Syed Hussain Abdul Hakeem**

- LinkedIn: https://www.linkedin.com/in/syed-hussain-abdul-hakeem
- GitHub: https://github.com/SyedHussain23

---

📄 License

This project is open source and available under the MIT License.

---

⭐ Show Your Support

If you found this project useful, consider giving it a ⭐.
