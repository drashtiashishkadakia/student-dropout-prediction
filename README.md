# Student Dropout & Graduation Prediction
**Machine Learning Project | BANA 3308 | 2024**

---

## Project Overview

Built a machine learning pipeline to predict whether university students will graduate or drop out based on personal, financial, and enrollment characteristics. The goal was to identify key risk factors that institutions can use to proactively support at-risk students.

---

## Problem Statement

Student dropout is a significant challenge for universities — it affects institutional performance, student outcomes, and resource allocation. This project uses historical student data to build predictive models that flag students at risk of dropping out before it's too late.

---

## Dataset

- **Records:** 3,300+ student entries
- **Features (8):** Age at enrollment, Gender, Scholarship holder status, Tuition fees up to date, International student status, Debtor status, Displaced status, Daytime/evening attendance
- **Target variable:** Graduate vs Dropout

---

## Methodology

### Tools
- **Orange Data Mining** — visual ML workflow tool
- **Models tested:** k-Nearest Neighbors (kNN) and Logistic Regression

### Pipeline
1. **Data Preparation** — loaded raw dataset, selected relevant features, removed outliers, imputed missing values
2. **Data Sampling** — split data into training and test sets using stratified sampling (66% train / 34% test)
3. **Model Training** — trained kNN and Logistic Regression models independently
4. **Evaluation** — compared models using AUC, accuracy, F1, precision, recall, and MCC
5. **Visualization** — built scatter plots and distribution charts to identify patterns

---

## Results

| Model | AUC | Accuracy | F1 | Precision | Recall |
|---|---|---|---|---|---|
| Logistic Regression | **0.814** | **75.5%** | 0.740 | 0.741 | 0.755 |
| kNN | 0.767 | 73.3% | 0.722 | 0.722 | 0.733 |

**Logistic Regression outperformed kNN across all metrics.**

### Confusion Matrix (Logistic Regression)
- Correctly predicted **1,493 graduates** out of 1,630 actual graduates
- Correctly predicted **506 dropouts** out of 1,019 actual dropouts
- Total test set: **2,649 records**

---

## Key Findings

- **Tuition fees up to date** — strongest predictor of graduation. Students with paid tuition showed overwhelmingly higher graduation rates
- **Scholarship holders** — significantly more likely to graduate
- **Evening class students** — slightly higher dropout tendency compared to daytime students
- **Age** — dropout tendency increases after age 35
- **Financial factors** (debt status, tuition) were collectively the most influential predictors

---

## Recommendations

Based on the findings, institutions should:
- Proactively reach out to students with outstanding tuition fees early in the semester
- Expand scholarship availability to reduce financial dropout risk
- Implement dedicated support programs for evening and part-time students
- Use predictive models like this to flag at-risk students for early intervention

---

## Files in this Repository

```
├── Student_Dropout_Prediction.ows    # Orange workflow file
├── images/
│   ├── workflow.png                  # Full ML pipeline in Orange
│   ├── test_score.png                # Model evaluation metrics
│   ├── confusion_matrix.png          # Logistic Regression confusion matrix
│   └── scatter_plot.png              # Tuition vs attendance scatter plot
└── README.md
```

---

## Contact

**Drashti Ashish Kadakia**
📧 drashtiashishkadakia@gmail.com
🔗 [linkedin.com/in/drashti-kadakia](https://linkedin.com/in/drashti-kadakia)
