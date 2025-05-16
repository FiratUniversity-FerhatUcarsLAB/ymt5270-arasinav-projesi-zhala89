# 📑 YMT5270 - Innovative Machine Learning Environments

## Midterm Project Report

**Student:** Zhala Sarkawt Othman

---

## 🗂️ 1. Dataset Selection

* **Dataset Name:** Mental Health in Tech Survey
* **Source:** [Kaggle - Mental Health in Tech Survey](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey)
* **License:** Open license (suitable for public educational use)
* **Original Collector:** Open Sourcing Mental Illness (OSMI) initiative
* **Total Samples (Rows):** 1,259
* **Total Features (Columns):** 26
* **Target Variable:** `treatment` (Yes/No) – indicating whether the individual has sought mental health treatment
* **Missing Data:** Approximately 2.4% across the dataset

This dataset was selected due to its relevance to real-world mental health issues in the tech industry and its suitability for classification tasks using Orange Data Mining.

---

## 🎯 2. Project Objective and Problem Type

* **Objective:** To build a machine learning model that predicts whether a tech employee has sought mental health treatment.
* **Machine Learning Task:** Classification
* **Tool Used:** Orange Data Mining (No programming required)

---

## 📊 3. Exploratory Data Analysis (EDA)

Using Orange Data Mining's visual widgets, the following steps were conducted:

* **Data Cleaning:**

  * Removed or ignored irrelevant columns such as `Timestamp`, `state`, and `Country`.
  * Set `treatment` as the target variable.

* **Missing Values:**

  * Imputation used to handle missing values in `Age`, `Gender`, and `work_interfere`.

* **Outlier Detection and Handling:**

  * Removed unrealistic age entries (e.g., age < 15 or > 80).

* **Class Balance:**

  * Moderate class imbalance observed in the target variable (`treatment`).

* **Correlation Analysis:**

  * `family_history` and `work_interfere` showed notable correlation with the target.

* **Visualization Techniques Used:**

  * Histograms, box plots, scatter plots, and feature distributions were explored.

---

## 🔧 4. Feature Selection

Features included in the modeling process:

* `Gender`
* `Age`
* `family_history`
* `work_interfere`
* `remote_work`
* `benefits`
* `care_options`
* `tech_company`

Columns such as `Timestamp`, `state`, and `Country` were excluded due to irrelevance or high cardinality with low predictive value.

---

## 🤖 5. Machine Learning Models Applied

Two supervised learning models were implemented using Orange:

* **Logistic Regression**
* **Random Forest Classifier**

Each model was evaluated using cross-validation with accuracy, AUC, F1 Score, precision, recall, and Matthews Correlation Coefficient (MCC) metrics.

---

## 📈 6. Evaluation and Performance Comparison

| Metric        | Logistic Regression | Random Forest |
| ------------- | ------------------- | ------------- |
| **AUC**       | 0.747               | 0.788         |
| **Accuracy**  | 65.9%               | 72.2%         |
| **F1 Score**  | 0.646               | 0.722         |
| **Precision** | 0.684               | 0.722         |
| **Recall**    | 0.659               | 0.722         |
| **MCC**       | 0.340               | 0.444         |

### Key Observations:

* **Best Performing Model:** Random Forest performed better across all evaluation metrics.
* **Most Influential Features:** `family_history`, `work_interfere`, and `benefits`.
* **Demographics Impact:** Gender and age had moderate influence, but work-related factors had higher predictive power.
* **Limitations Identified:**

  * Class imbalance and missing values slightly impacted performance.
  * Inconsistent entries in `Gender` and `Age` reduced model clarity.

---

## 🧠 7. Interpretation of Results

* **Model Insight:** Random Forest was more effective in capturing nonlinear relationships in the data, leading to better classification accuracy.
* **Feature Insight:** Indicators related to workplace support (`benefits`, `care_options`, `work_interfere`) and personal background (`family_history`) were crucial in predicting mental health treatment.
* **Data Quality Impact:** Missing data and demographic inconsistency (especially in gender entries) posed a challenge, but imputation and cleaning improved performance.

---

## ✅ 8. Conclusion

This project successfully demonstrated how Orange Data Mining can be used to perform end-to-end machine learning without writing any code. The platform's intuitive visual interface enabled efficient data preprocessing, visualization, and model evaluation.

* **Recommended Model:** Random Forest
* **Future Work:**

  * Use SMOTE or other resampling techniques to handle class imbalance.
  * Consider refining gender and age categories for better consistency.

---

## 📁 9. Submitted Files

* ✅ `ReadMe_YourProject.md` (completed based on provided template)
* ✅ Orange workflow file (`.ows`)
* ✅ Dataset link: [Kaggle Dataset](https://www.kaggle.com/datasets/osmi/mental-health-in-tech-survey)

---


## ✉️ Contact

For any project-related questions: **[zhala.sarkawt@gmail.com]**

