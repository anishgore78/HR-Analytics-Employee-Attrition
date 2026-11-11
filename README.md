# HR Analytics – Employee Attrition Analysis

## Project Overview

Employee attrition is a major challenge for organizations because frequent employee turnover can increase recruitment costs, reduce productivity, and affect workforce planning.

This project focuses on analyzing employee attrition using Python, statistical techniques, data visualization, and machine learning. The objective is to identify factors associated with employee turnover, understand employee behavior, and build a predictive model that can help HR teams make data-driven retention decisions.

## Objectives

- Analyze employee demographics and job-related characteristics.
- Identify patterns and trends associated with employee attrition.
- Study the impact of overtime, job satisfaction, work-life balance, and other factors on attrition.
- Perform statistical hypothesis testing to identify significant associations.
- Build a Logistic Regression model to predict employee attrition.
- Generate actionable business insights and HR recommendations.

## Dataset

The project uses an HR Analytics employee dataset containing demographic, professional, and workplace-related information.

**Dataset details:**
- Original records: 1,480
- Original features: 38
- Records after cleaning: 1,416
- Features after feature engineering: 39
- Employees who left: 229
- Overall attrition rate: 16.17%

Data preprocessing included handling missing values, removing exact duplicate records, and creating a new feature called `TenureGroup` based on years at the company.

## Tools and Technologies

- **Python** – Programming language
- **Pandas & NumPy** – Data manipulation and analysis
- **Matplotlib & Seaborn** – Data visualization
- **SciPy** – Statistical hypothesis testing
- **Scikit-learn** – Machine learning and model evaluation
- **Google Colab** – Development environment
- **Jupyter Notebook** – Interactive analysis

## Project Workflow

1. Data Loading and Initial Inspection
2. Data Cleaning and Preprocessing
3. Exploratory Data Analysis (EDA)
4. Correlation Analysis
5. Statistical Hypothesis Testing
6. Logistic Regression Model Development
7. Model Evaluation
8. Business Insights and HR Recommendations

## Exploratory Data Analysis

EDA was performed to understand employee attrition across different categories, including:

- Department and gender
- Age groups
- Salary slabs
- Years at the company
- Job roles
- Job satisfaction
- Environment satisfaction
- Work-life balance

## Statistical Hypothesis Testing

Chi-Square tests of independence were used to examine the association between employee attrition and selected categorical variables.

Cramér's V was used to measure the strength of these associations.

**Key findings:**

| Factor | Cramér's V |
|---|---:|
| Overtime | 0.2504 |
| Environment Satisfaction | 0.1240 |
| Work-Life Balance | 0.1091 |
| Job Satisfaction | 0.1059 |
| Department | 0.0879 |

Overtime showed the strongest association with employee attrition among the tested factors.

## Machine Learning Model

A Logistic Regression model was developed to predict employee attrition.

**Model development steps:**
- Categorical feature encoding using One-Hot Encoding.
- Numerical feature scaling using StandardScaler.
- Train-test split with an 80:20 ratio.
- Stratified sampling to maintain class distribution.
- Class balancing using `class_weight='balanced'`.

### Model Performance

| Evaluation Metric | Score |
|---|---:|
| Accuracy | 75.00% |
| Precision | 35.96% |
| Recall | 69.57% |
| F1-Score | 47.41% |
| ROC-AUC | 80.75% |

The model achieved a ROC-AUC score of approximately 0.81 and a recall of 69.57%, indicating its ability to identify a considerable proportion of employees who left.

The model also uses a balanced class-weight setting to address the imbalance between employees who stayed and employees who left.

## Key Business Insights

- Employees working overtime showed a considerably higher attrition rate.
- Lower job satisfaction was associated with higher employee attrition.
- Employees reporting poor work-life balance showed higher attrition.
- Attrition rates varied across departments and job roles.
- Employees with shorter company tenure showed comparatively higher attrition.

## HR Recommendations

- Monitor employee overtime and workload distribution.
- Improve employee engagement and job satisfaction.
- Encourage a healthier work-life balance.
- Develop targeted retention strategies for high-attrition job roles.
- Strengthen onboarding and support for new employees.
- Use predictive analytics to support employee retention planning.

## Project Structure

```text
HR-Analytics-Employee-Attrition/
│
├── HR_Analytics__EDA(1).ipynb
├── HR Analytics dataset (1).xlsx
└── README.md
```

## How to Run the Project

1. Clone this repository:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

2. Open the project in Google Colab or Jupyter Notebook.

3. Upload the dataset or update the dataset path in the notebook.

4. Install the required libraries if they are not already available:

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn openpyxl
```

5. Run the notebook cells sequentially to reproduce the analysis and model evaluation.

## Future Scope

- Implement advanced machine learning models such as Random Forest and XGBoost.
- Perform hyperparameter tuning to improve model performance.
- Apply explainable AI techniques such as SHAP to understand model predictions.
- Develop an interactive HR analytics dashboard.
- Explore additional employee engagement indicators for better attrition prediction.

## Conclusion

This project demonstrates how data analytics, statistical hypothesis testing, and machine learning can be used to understand employee attrition.

The analysis identifies overtime as an important factor associated with employee turnover and highlights the importance of employee satisfaction and work-life balance. The Logistic Regression model provides a predictive approach that can support HR teams in identifying potential attrition risks and developing employee retention strategies.
