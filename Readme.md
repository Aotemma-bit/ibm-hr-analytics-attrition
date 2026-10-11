# IBM HR Analytics — Employee Attrition Analysis

**Data Science Capstone Project | Group 2**

## Project Overview

This project analyzes employee attrition using the IBM HR Analytics Employee Attrition dataset. The objective is to explore factors associated with employees leaving an organization, identify workforce patterns, and build machine learning models that can help HR teams better understand attrition risk.

The project combines data cleaning, SQL analysis, exploratory data analysis, feature engineering, clustering, and predictive modeling.

## Business Problem

Employee attrition can create recruitment costs, disrupt operations, and result in the loss of experienced employees.

Organizations need to understand which workforce characteristics are associated with attrition and how data can support better workforce planning.

This project investigates employee attrition patterns and evaluates machine learning approaches for identifying employees who may be at higher risk of leaving.

## Project Objectives

- Analyze employee attrition patterns across workforce categories.
- Explore relationships between employee characteristics and attrition.
- Clean and prepare the dataset for analysis.
- Engineer additional features to support modeling.
- Apply clustering to identify employee segments.
- Build and compare classification models.
- Evaluate model performance using appropriate classification metrics.
- Translate analytical findings into practical HR insights.

## Dataset

The project uses the **IBM HR Analytics Employee Attrition & Performance** dataset.

The dataset contains employee-related information, including:

- Age and marital status
- Department and job role
- Monthly income
- Business travel frequency
- Years at the company
- Years in the current role
- Job satisfaction and work-life balance
- Overtime status
- Employee attrition status

The dataset contains 1,470 employee records before cleaning.

## Tools and Technologies

- **Python** — data analysis and machine learning
- **Pandas and NumPy** — data manipulation
- **SQL** — workforce analysis and aggregation
- **Matplotlib and Seaborn** — data visualization
- **Scikit-learn** — clustering, classification, preprocessing, and evaluation
- **Google Colab / Jupyter Notebook** — development environment

## Methodology

### 1. Data Cleaning

The dataset was inspected for missing values, duplicate records, constant columns, and potential identifier fields.

### 2. Exploratory Data Analysis

Workforce characteristics were explored to identify patterns associated with employee attrition.

### 3. SQL Analysis

SQL aggregation was used to examine attrition across business travel categories.

### 4. Feature Engineering

Additional features were created, including tenure categories, prior-company counts, and a role-tenure ratio.

### 5. Clustering

K-means clustering was applied to standardized workforce features to explore employee segments. Silhouette scores were compared across different values of K.

### 6. Predictive Modeling

The following classification approaches were evaluated:

- Dummy Classifier baseline
- Logistic Regression
- Class-weighted Logistic Regression
- Random Forest
- Gradient Boosting
- SMOTE combined with Logistic Regression

### 7. Model Evaluation

Models were compared using accuracy, precision, recall, F1-score, and ROC AUC. Cross-validation and a held-out test set were used for model assessment.

Because attrition is an imbalanced classification problem, the analysis considers the trade-off between identifying employees who leave and incorrectly flagging employees who stay.

## Selected Findings

### Attrition and Business Travel

The SQL analysis produced the following results:

| Business Travel Category | Employees | Employees Who Left | Attrition Rate |
|---|---:|---:|---:|
| Travel Frequently | 277 | 69 | 24.91% |
| Travel Rarely | 1,043 | 156 | 14.96% |
| Non-Travel | 150 | 12 | 8.00% |

In this dataset, employees who travelled frequently had the highest observed attrition rate among these three categories. This is an association in the dataset and does not establish that business travel causes attrition.

### Clustering

K-means clustering was evaluated using silhouette scores. Among the tested configurations, two clusters achieved the highest reported silhouette score of approximately 0.127.

The resulting clusters showed differences in age, income, and tenure characteristics.

### Classification

Logistic Regression and alternative classification approaches were evaluated against a baseline. Class weighting and SMOTE were also explored to address the imbalance between employees who stayed and those who left.

The project emphasizes recall, precision, F1-score, and ROC AUC alongside accuracy because accuracy alone can obscure poor performance on the minority attrition class.

## Business Implications

The analysis illustrates how HR analytics can support:

- Workforce attrition monitoring
- Identification of patterns associated with employee turnover
- Employee segmentation for further investigation
- Evidence-based workforce planning
- Evaluation of predictive models for HR decision support

Any model-generated risk score should be treated as an analytical signal for further review, not as a definitive judgment about an employee. Predictions should not be used as the sole basis for employment decisions.

## Repository Contents

- `GROUP__2_TOBILOBA__ABIODUN.ipynb` — the project notebook containing the analysis, visualizations, clustering, and classification experiments.
- `README.md` — project overview, methodology, and selected findings.

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Ensure the required Python libraries are installed.
3. Make the dataset available at the file path expected by the notebook.
4. Run the notebook cells in order.
5. Review the analysis, visualizations, and model evaluation results.

## Limitations

- The analysis uses a single HR analytics dataset and may not generalize to every organization.
- Observed relationships do not establish causation.
- Predictive performance depends on the available features, model assumptions, and evaluation method.
- Attrition predictions require careful consideration of privacy, fairness, and appropriate use.

## Conclusion

This capstone project demonstrates an end-to-end data science workflow for employee attrition analysis, from data preparation and SQL exploration to clustering and predictive modeling.

It highlights how workforce data can be transformed into interpretable insights and how machine learning models can be evaluated for potential HR analytics applications.

---

**Project:** IBM HR Analytics — Employee Attrition Analysis  
**Track:** Data Science  
**Team:** Group 2  
**Author:** Tobi Abiodun

