
# 📘 Comparing Classifiers

### Module-17: Practical Exercise-3

The goal of this assignment is to compare the performance of classifiers:  
**k-nearest neighbors, logistic regression, decision trees, and support vector machines.**

We use a dataset related to the marketing of bank products over the telephone.

---

## 📂 Dataset

- From: [UCI Machine Learning Repository - Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing)  
- Data from a **Portuguese Banking Institution**, collected over **17 marketing campaigns** (May 2008 to Nov 2010)

---

## 📏 Measurement Criteria

The project structure is under the GitHub repository:  
`Comparing_Classifiers_Portuguese_Bnk`

---

## 📈 CRISP-DM Application (Six Phases)

### 1. Business Understanding

**Objective:**  
Predict whether a bank client will subscribe to a term deposit based on information from direct marketing (e.g., phone calls), demographic, and economic context.

### 2. Data Understanding

- **41188 entries**, **21 attributes**

#### Input Features:

- **Bank Client Data**
  - `age` (numeric)
  - `job`, `marital`, `education`, `default`, `housing`, `loan` (categorical)

- **Contact Info**
  - `contact`, `month`, `day_of_week`, `duration`

- **Campaign-related**
  - `campaign`, `pdays`, `previous`, `poutcome`

- **Economic Context**
  - `emp.var.rate`, `cons.price.idx`, `cons.conf.idx`, `euribor3m`, `nr.employed`

#### Output Variable:
- `y`: Client subscribed to a term deposit? (`yes` or `no`)

---

### 3. Data Preparation

- Replace `'unknown'` with `NaN`
- Drop `duration` (leaks target)
- Convert categorical → one-hot encoding
- Scale/normalize numeric features
- Split into training and test sets

---

### 4. Modeling

Models used:

- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Support Vector Machine

#### Baseline Accuracy: `88.73%`

---

## 📊 Model Comparison Summary

| Model                  | Train-Time (s) | Train Accuracy | Test Accuracy |
|------------------------|----------------|----------------|----------------|
| Logistic Regression    | 0.2437         | 90.02%         | **90.13%** ✅ |
| K-Nearest Neighbors    | 0.0062         | 91.24%         | 89.33%         |
| Decision Tree          | 0.4174         | **99.47%**     | 84.07% ❌      |
| Support Vector Machine | 343.4604       | 90.91%         | 90.08%         |

---

## 📉 Visualizations

- Accuracy Comparison Plot  
- ROC Curve Comparison  
- Confusion Matrix (SVM excluded from plots due to long training time)

---

## ✅ Recommendations

### Logistic Regression — ✅ **Recommended**
- Best accuracy + fastest
- Interpretable and efficient

### Support Vector Machine — ⚠️ **Strong but Costly**
- High accuracy, but **very slow** to train

### K-Nearest Neighbors — ⚠️ **Good but Not Scalable**
- Decent accuracy, but slow at prediction time

### Decision Tree — ❌ **Not Reliable**
- Overfitting observed (train acc 99.4%, test acc 84%)

> Suggest using **Random Forest or Gradient Boosting** instead of plain Decision Trees.

---

## 📌 Final Recommendation Summary

| Use Case                        | Best Model           | Notes                                       |
|----------------------------------|------------------------|---------------------------------------------|
| Fast, interpretable, reliable   | Logistic Regression   | ✅ Best all-around performer                |
| Slightly better generalization | SVM                   | ⚠️ Slower and harder to explain            |
| Simplicity, no training time   | KNN                   | Use for small-scale or educational purposes |
| Rule-based logic               | Random Forest (future)| Better than plain trees                     |

---

## 🧾 Conclusion

**✅ Prediction Goal Met**  
Models can reasonably predict term deposit subscription (`yes` or `no`) using client, campaign, and economic context data.

**Best Model: Logistic Regression**
- ~90% test accuracy
- Fast, interpretable
- Suitable for real-world deployment

---

## 🔒 Cisco Confidential
