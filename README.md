# Predicting Employee Attrition using Machine Learning

This project aims to predict employee attrition using machine learning techniques. The dataset for this analysis has been sourced from Kaggle. Key machine learning models such as Decision Tree, Random Forest, and Gradient Boosting have been employed to create and evaluate the predictions.

## Data Preprocessing

### Binary Encoding
The following binary columns were encoded as 1/0 for efficient model training:

- **Attrition**: `1` for "Yes", `0` for "No".
- **Gender**: `1` for "Male", `0` for "Female".
- **Over18**: `1` for "Y", `0` for others.
- **OverTime**: `1` for "Yes", `0` for "No".

### One-Hot Encoding

The following categorical columns were one-hot encoded using pandas `get_dummies()` function:

- **BusinessTravel**
- **MaritalStatus**
- **JobRole**
- **EducationField**
- **Department**

### Removal of Irrelevant Columns

Columns that had no significant contribution to the analysis, such as those with a single distinct value, were removed:

- **EmployeeCount**
- **StandardHours**
- **Over18**
## Model Performance

The following machine learning models were used, and their accuracy scores are:

| Model                        | Accuracy  |
|------------------------------|-----------|
| Decision Tree Classifier     | 76.87%    |
| Random Forest Classifier     | 86.05%    |
| Gradient Boosting Classifier | 87.41%    |

## Feature Importances (Random Forest)

The following table shows the feature importances as identified by the Random Forest model:

| Feature                             | Importance |
|-------------------------------------|------------|
| MonthlyIncome                       | 0.0753     |
| Age                                 | 0.0595     |
| TotalWorkingYears                   | 0.0521     |
| DailyRate                           | 0.0495     |
| OverTime                             | 0.0468     |
| MonthlyRate                          | 0.0462     |
| HourlyRate                           | 0.0453     |
| DistanceFromHome                     | 0.0439     |
| YearsAtCompany                       | 0.0401     |
| NumCompaniesWorked                   | 0.0347     |
| PercentSalaryHike                    | 0.0340     |
| JobInvolvement                       | 0.0290     |
| YearsWithCurrManager                 | 0.0285     |
| StockOptionLevel                     | 0.0284     |
| YearsInCurrentRole                   | 0.0269     |
| EnvironmentSatisfaction              | 0.0265     |
| TrainingTimesLastYear                | 0.0263     |
| JobSatisfaction                      | 0.0263     |
| WorkLifeBalance                      | 0.0253     |
| YearsSinceLastPromotion              | 0.0229     |
| RelationshipSatisfaction             | 0.0208     |
| JobLevel                             | 0.0200     |
| Education                            | 0.0170     |
| MaritalStatus_Single                 | 0.0167     |
| Travel_Frequently                    | 0.0164     |
| MaritalStatus_Married                | 0.0106     |
| Gender                               | 0.0099     |
| Field_Technical Degree               | 0.0094     |
| Field_Medical                        | 0.0090     |
| Department_Research & Development    | 0.0088     |
| Role_Laboratory Technician           | 0.0085     |
| Role_Sales Representative            | 0.0082     |
| Role_Sales Executive                 | 0.0076     |
| Travel_Rarely                        | 0.0075     |
| Role_Research Scientist              | 0.0075     |
| Department_Sales                     | 0.0074     |
| MaritalStatus_Divorced               | 0.0070     |
| Field_Life Sciences                  | 0.0068     |
| Field_Marketing                      | 0.0060     |
| PerformanceRating                    | 0.0051     |
| Role_Manufacturing Director          | 0.0035     |
| Non-Travel                           | 0.0032     |
| Role_Human Resources                 | 0.0030     |
| Department_Human Resources           | 0.0028     |
| Field_Other                          | 0.0027     |
| Role_Healthcare Representative       | 0.0027     |
| Field_Human Resources                | 0.0020     |
| Role_Manager                         | 0.0015     |
| Role_Research Director               | 0.0009     |

This table provides a clear representation of feature importances, making it easy to understand which features are most influential in the Random Forest model.


