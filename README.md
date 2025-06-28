# 🧬 Breast Cancer Detection with Machine Learning
  ## Predicting malignant vs benign tumors with high precision using logistic regression and advanced threshold tuning.
  ## 🚀 Overview
  This project builds a reliable machine learning pipeline to classify breast tumors as *malignant (cancerous)* or *benign (non-cancerous)* using diagnostic features from    the well-known [Wisconsin Breast Cancer Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29).

  With a strong focus on *recall* (minimizing false negatives), the model achieves:

- ✅ *Accuracy:* 98%
- ✅ *ROC AUC:* 0.995
- ✅ *No false negatives* at the tuned threshold (0.3)

## 🧠 Key Highlights

- ✅ End-to-end ML pipeline (data cleaning, scaling, modeling, evaluation)  
- 🎯 Threshold tuning to prioritize *recall* (critical in medical diagnosis)  
- 📈 ROC & Precision-Recall curve analysis  
- 🔍 Feature importance analysis from logistic regression  
- 📂 Exported performance plots & metrics  
## 📊 Model Evaluation & Results

### 🔍 At Default Threshold (0.5)

| Metric    | Malignant (0) | Benign (1) |
|-----------|----------------|------------|
| Precision | 0.98           | 0.99       |
| Recall    | 0.98           | 0.99       |
| F1-score  | 0.98           | 0.99       |

*Accuracy:* 0.98  
*ROC AUC Score:* 0.9954  
*Confusion Matrix:*
[[41  1] [ 1  71]]

![roc_curve](https://github.com/user-attachments/assets/05f3cfc4-fbb6-40d8-914a-2a39c03e9727)

### ⚖️ Tuned Threshold (0.3) — Maximizing Recall

| Metric    | Malignant (0) | Benign (1) |
|-----------|----------------|------------|
| Precision | 1.00           | 0.97       |
| Recall    | 0.95           | 1.00       |

*Confusion Matrix:*

[[40  2] [ 0 72]]

📌 At this threshold, *no cancer cases were missed* — ideal for medical diagnosis scenarios.
![precision_recall_vs_threshold](https://github.com/user-attachments/assets/f0424cf9-d06b-4770-af59-aec7b0898f4f)

### 🔬 Top 10 Influential Features (Logistic Regression)

| Rank | Feature                | Coefficient |
|------|------------------------|-------------|
| 1    | texture_worst          | -1.25       |
| 2    | radius_se              | -1.08       |
| 3    | concave points_worst   | -0.95       |
| 4    | area_worst             | -0.94       |
| 5    | radius_worst           | -0.94       |
| 6    | symmetry_worst         | -0.93       |
| 7    | area_se                | -0.92       |
| 8    | concavity_worst        | -0.82       |
| 9    | perimeter_worst        | -0.76       |
| 10   | smoothness_worst       | -0.74       |
🧠 These features contribute most to the classification decision. Higher negative values are strongly linked to malignancy.

## 🛠️ Tech Stack

- Python 3.9+
- Scikit-learn
- Pandas, NumPy
- Matplotlib, Seaborn
  
## 💡 Use Cases
🧬 Early cancer detection tools
🏥 Medical diagnostic support systems
🎓 Teaching healthcare professionals how ML models work

## 🤝 Contributions
 Open to collaboration! If you'd like to:
 Add cross-validation
 Improve generalization
 Use neural networks or ensemble methods
 Feel free to open a PR or raise an issue!


## 📜 License
This project is under the MIT License — feel free to use, modify, and distribute with proper attribution.

## 💬 Final Thoughts
 Machine learning can save lives — when used responsibly.
 This project shows how careful threshold selection, interpretability, and domain context create a trustworthy ML solution for healthcare.
