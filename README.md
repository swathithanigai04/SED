# SED
Overview

This project presents a comprehensive data-driven approach to analyzing student behavior and predicting academic outcomes using the Student Engagement Dataset (SED). The system integrates machine learning techniques to identify at-risk students, predict marks and engagement scores, cluster behavioral patterns, and detect potential withdrawals. It is designed to support early interventions, enhance faculty decision-making, and improve overall academic engagement in online learning environments.

Objectives

1. Predict students at risk of academic failure.
2. Classify students into grade bands (A–F).
3. Cluster students based on engagement behaviors using unsupervised learning.
4. Predict academic scores and engagement scores using regression models.
5. Analyze faculty performance across departments.
6. Detect potential student withdrawals or dropouts based on LMS behavior.

Dataset
Source:

Student Engagement Dataset (SED) – Universiti Malaya LMS (12M+ rows, 4 files)

Files Used:

1. Student_log.csv – Raw student activity logs (timestamped)
2. Student_activity_summary.csv – Aggregated login and engagement features
3. Student_grade_aggregated.csv – Total marks and courses per student
4. Student_grade_detailed.csv – Course-level grades and faculty data

Technologies Used

1. Python - Core programming language
2. Pandas, NumPy - Data manipulation and aggregation
3. Matplotlib, Seaborn - Visual analytics and pattern exploration
4. Scikit-learn -	Machine learning models (classification, regression, clustering)
5. Jupyter Notebook - Interactive modeling and visual reporting

Key ML Techniques
Classification
1. At-Risk Prediction: Binary classification (avg mark < 50)
2. Grade Band Classification: A, B, C, D, F labeling using predicted marks

Regression
1. Marks Prediction: Predict normalized average marks per student
2. Engagement Score Prediction: Model behavior-driven engagement index

Clustering
1. K-Means Clustering: Behavioral grouping (e.g., High vs Low Engagement)
2. Silhouette Score used for optimal k-selection and validation

Correlation & Behavioral Analysis
1. Spearman Correlation between engagement metrics and grades
2. Mann–Whitney U Test to compare top/bottom performer patterns

Faculty Performance Analysis
1. Aggregate faculty-wise metrics (avg mark, std deviation, number of students)
2. Visualization using dual-axis charts (bar & line plots)

Dropout Prediction (Simulated)
1. Withdrawal labels based on actual grade codes (W, I, CN, etc.)
2. Classifier trained on features like zero quiz completion and low logins

Visualizations Included
1. Feature correlation heatmaps
2. Cluster profile box plots
3. Grade band confusion matrix
4. Time series login patterns
5. Faculty performance charts
6. Histograms of quiz ratios and logins

Feature Engineering
Derived over 15 features from raw LMS logs, including:

1. engagement_score
2. quiz_completion_ratio
3. login_per_course
4. weekend_weekday_ratio
5. late_vs_early_login
6. marks_per_course, assignments_per_course
7. cluster_label (High/Low Engagement)

Insights & Outcomes
1. At-Risk classification achieved ~99% F1-score
2. Academic marks predicted with R² ≈ 0.99
3. Engagement clusters revealed significant academic differences
4. Faculty analysis exposed disparities in student outcomes across departments
5. Early indicators of student withdrawal based on LMS inactivity
