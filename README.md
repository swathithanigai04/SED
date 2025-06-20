## Overview

This project presents a comprehensive data-driven approach to analyzing student behavior and predicting academic outcomes using the **Student Engagement Dataset (SED)**. The system integrates **machine learning** techniques to identify **at-risk students**, **predict marks and engagement scores**, **cluster behavioral patterns**, and **detect potential withdrawals**. It is designed to support **early interventions**, enhance **faculty decision-making**, and improve overall academic engagement in **online learning environments**.


## Objectives

* Predict students at risk of academic failure.
* Classify students into **grade bands** (A–F).
* Cluster students based on **engagement behaviors** using unsupervised learning.
* Predict **academic scores** and **engagement scores** using regression models.
* Analyze faculty performance across departments.
* Detect potential student **withdrawals or dropouts** based on LMS behavior.


## Dataset

**Source:**
Student Engagement Dataset (SED) – Universiti Malaya LMS (12M+ rows, 4 files)

**Files Used:**

* `Student_log.csv` – Raw student activity logs (timestamped)
* `Student_activity_summary.csv` – Aggregated login and engagement features
* `Student_grade_aggregated.csv` – Total marks and courses per student
* `Student_grade_detailed.csv` – Course-level grades and faculty data

## Technologies Used

| Tool/Library            | Purpose                                                          |
| ----------------------- | ---------------------------------------------------------------- |
| **Python**              | Core programming language                                        |
| **Pandas, NumPy**       | Data manipulation and aggregation                                |
| **Matplotlib, Seaborn** | Visual analytics and pattern exploration                         |
| **Scikit-learn**        | Machine learning models (classification, regression, clustering) |
| **Jupyter Notebook**    | Interactive modeling and visual reporting                        |

## Key ML Techniques

### Classification

* **At-Risk Prediction**: Binary classification (avg mark < 50)
* **Grade Band Classification**: A, B, C, D, F labeling using predicted marks

### Regression

* **Marks Prediction**: Predict normalized average marks per student
* **Engagement Score Prediction**: Model behavior-driven engagement index

### Clustering

* **K-Means Clustering**: Behavioral grouping (e.g., High vs Low Engagement)
* **Silhouette Score** used for optimal k-selection and validation

### Correlation & Behavioral Analysis

* **Spearman Correlation** between engagement metrics and grades
* **Mann–Whitney U Test** to compare top/bottom performer patterns

### Faculty Performance Analysis

* Aggregate faculty-wise metrics (avg mark, std deviation, number of students)
* Visualization using dual-axis charts (bar & line plots)

### Dropout Prediction (Simulated)

* Withdrawal labels based on actual grade codes (`W`, `I`, `CN`, etc.)
* Classifier trained on features like zero quiz completion and low logins

## Visualizations Included

* Feature correlation heatmaps
* Cluster profile box plots
* Grade band confusion matrix
* Time series login patterns
* Faculty performance charts
* Histograms of quiz ratios and logins

## Feature Engineering

Derived over **15 features** from raw LMS logs, including:

* `engagement_score`
* `quiz_completion_ratio`
* `login_per_course`
* `weekend_weekday_ratio`
* `late_vs_early_login`
* `marks_per_course`, `assignments_per_course`
* `cluster_label` (High/Low Engagement)

## Insights & Outcomes

* At-Risk classification achieved **\~99% F1-score**
* Academic marks predicted with **R² ≈ 0.99**
* Engagement clusters revealed significant academic differences
* Faculty analysis exposed disparities in student outcomes across departments
* Early indicators of student withdrawal based on LMS inactivity

## 📄 Citation
> Z. H. Azizul, M. S. S. Kassim, and A. A. H. Ahmad Fuaad, “Student Engagement Dataset (SED): An Online Learning Activity Dataset,” IEEE Access, vol. 13, 2025, doi: 10.1109/ACCESS.2025.3531102.
