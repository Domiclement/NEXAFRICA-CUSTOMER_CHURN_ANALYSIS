# Customer Churn Prediction
**NexAfrica Machine Learning Project**  


## Project Overview
This project applies machine learning to telecommunications customer churn prediction. It explores customer behavior, compares classification models, examines feature importance, and translates observed patterns into business recommendations.

## Business Problem
Customer churn can reduce recurring revenue and increase acquisition costs. This project investigates whether customer and service information can help identify customers at risk of leaving and support targeted retention efforts.

## Dataset
The Telco Customer Churn dataset contains 7,043 original customer records and 21 columns. After cleaning, the notebook reports 7,032 records: 1,869 churned and 5,163 stayed, an observed churn rate of 26.58%. The target is `Churn`.

## Tools and Technologies
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, Google Colab/Jupyter, Git and GitHub.

## Project Workflow
1. Business understanding
2. Data collection
3. Data understanding
4. Data cleaning
5. Exploratory data analysis
6. Feature engineering
7. Data preprocessing
8. Model development
9. Model evaluation
10. Class-imbalance handling
11. Hyperparameter tuning
12. Final model selection
13. Feature importance
14. Business insights
15. Recommendations
16. Conclusion

## Exploratory Data Analysis
EDA examined churn distribution, contracts, tenure, internet service, billing, and support-related services. The cleaned dataset's observed churn rate was 26.58%. Churn rates also differed across contract and service categories in the test sample.

## Machine Learning Models
Logistic Regression, Decision Tree, Random Forest, and XGBoost were compared. Random Forest was confirmed as the final model based on the reported highest F1-score and a recall of 72.46%.

## Evaluation Metrics
- **Accuracy:** proportion of all predictions that are correct.
- **Precision:** proportion of predicted churners who actually churn.
- **Recall:** proportion of actual churners identified.
- **F1-score:** harmonic mean of precision and recall.
- **ROC-AUC:** ability to distinguish churners from non-churners across thresholds.
- **Confusion matrix:** counts of true positives, true negatives, false positives, and false negatives.

### Reported model comparison
| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Random Forest | 76.83% | 54.86% | 72.46% | 62.44% | 0.8309 |
| Logistic Regression | 72.64% | 49.09% | 79.68% | 60.75% | 0.8339 |
| Decision Tree | 74.41% | 51.32% | 72.99% | 60.26% | 0.8168 |
| XGBoost | 79.32% | 63.52% | 52.14% | 57.27% | 0.8358 |

## Key Findings
Random Forest permutation importance ranked Contract (about 0.084 decrease in F1), Tenure (0.072), InternetService (0.030), MonthlyCharges (0.026), and MultipleLines (0.015) as the leading features. Values are approximate readings from the project chart.

Observed churn rates in the test sample:
- Month-to-month contract: 41.27% (326/790)
- One-year contract: 13.79% (40/290)
- Two-year contract: 2.45% (8/327)
- No technical support: 41.23% (294/713); with technical support: 7.69% (24/312)
- No online security: 41.35% (287/694); with online security: 7.69% (24/312)
- Fiber optic: 42.25% (259/613); DSL: 18.88% (91/482); no internet service: 7.69% (24/312)

These are observed associations, not proof of causation.

## Business Recommendations
1. Investigate higher churn among month-to-month customers and test suitable longer-term contract offers.
2. Examine churn across tenure bands and test onboarding or early-engagement interventions.
3. Investigate fiber-optic customer experience, including reliability, pricing, complaints, and satisfaction.
4. Review technical support access, response times, and complaint resolution.
5. Evaluate online-security awareness, adoption, and perceived value.
6. Use predicted churn probabilities to prioritize retention outreach while monitoring false positives and false negatives.
7. Measure retention rates, campaign costs, and revenue retained to assess intervention value.

## Conclusion
The project demonstrates a machine-learning workflow for churn prediction and links model findings to possible retention actions. Contract and tenure were the leading features in the reported Random Forest importance analysis. Before operational use, validate on new data, review error costs, and test retention interventions.
