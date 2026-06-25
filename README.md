
<h2>Telco Customer Churn Analysis</h2>
<h3>Project Overview</h3>
This project focuses on analyzing and predicting customer churn in a telecommunications company using machine learning techniques. The goal is to identify factors contributing to customer attrition and characterize customers who are likely to churn versus those who are likely to be retained. This understanding can help in developing targeted retention strategies and improving customer satisfaction.
Used data from Kaggle based on Telco Customer Data to generate a predcition analysis with churn.

**Dataset**<br>
The analysis utilizes the Telco Customer Churn(WA_Fn-UseC_-Telco-Customer-Churn.csv) dataset generated from Kaggle, which contains information about a telecommunication company's customers, including their services, account information, and whether they churned or not.

**Methodology**<br>
The project involved several key steps:<br>

- Data Loading & Initial Exploration: Loaded the dataset and performed initial checks on data types and missing values.
- Data Preprocessing & Feature Engineering:
- Handled missing values in TotalCharges by converting it to a numeric type and imputing with the median.
- Dropped the customerID as it's an irrelevant identifier for modeling.
- Encoded binary categorical features (like gender, Partner, Dependents, Churn) using LabelEncoder.
- Applied OneHotEncoder to multi-category nominal features (e.g., MultipleLines, InternetService, Contract, PaymentMethod).
- Scaled numerical features (tenure, MonthlyCharges, TotalCharges) using StandardScaler.
- Model Training: Split the preprocessed data into training and testing sets. A Logistic Regression model was trained on the training data.
- Model Evaluation: Evaluated the model's performance using a classification_report (precision, recall, F1-score) and a confusion_matrix.
- Customer Profiling & Visualization: Identified customers predicted to be retained and churned.
  <br>
Visualized characteristics of both groups, including distributions of numerical features **(tenure, MonthlyCharges, TotalCharges)** and proportions of various categorical features **(e.g., SeniorCitizen status, Contract type, InternetService, PaymentMethod, Gender, Partner status, Dependents status, OnlineSecurity usage)**.
<br>**Key Insights**<br>
General Model Performance
The Logistic Regression model achieved an accuracy of approximately 80.5% on the test set. Detailed precision, recall, and F1-scores were examined, showing the model's ability to identify both churned and non-churned customers.
  
**Characteristics of Retained Customers**<br>
Customers predicted to be retained generally exhibited:

- Higher Tenure: Tend to have been customers for a longer duration.
- Higher Total Charges: Accumulated greater total charges, aligning with longer tenure.
- Contract Types: A higher proportion of customers with One year or Two year contracts.
- Demographics: Distinct distributions across gender, Partner status, Dependents status, and SeniorCitizen status.
- Service Usage: Specific preferences for InternetService types, PaymentMethods, and OnlineSecurity service usage.
  **Characteristics of Churned Customers**<br>
Customers predicted to churn typically showed:

- Lower Tenure: Often leave early in their customer lifecycle.
- Lower Total Charges: Consistent with shorter tenure.
- Contract Types: A significantly higher proportion of customers on Month-to-month contracts.
- Service Usage: Overrepresentation of Fiber optic internet service and Electronic check payment method, suggesting potential dissatisfaction with these aspects.
- Online Security: A notable number of churned customers did not use 'Online Security' service.<br>
  These insights suggest that factors like contract length, specific internet services, payment methods, and initial customer engagement play crucial roles in customer retention. The model provides a robust framework for identifying at-risk customers.

**Technologies Used**
- Python
- pandas (for data manipulation and analysis)
- numpy (for numerical operations)
- scikit-learn (for machine learning, preprocessing, and model evaluation)
- matplotlib (for data visualization)
- seaborn (for enhanced data visualization)
