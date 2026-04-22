# Prediction-Model
Customer Churn Prediction Model

Case Study Overview

This project focuses on building a customer churn prediction model that leverages historical customer data to estimate the likelihood of customers discontinuing a service.

Churn prediction models analyze patterns in customer behavior, including product usage and direct feedback, to identify signals that indicate whether a customer is likely to stay or leave. These insights enable businesses to take proactive measures to improve retention.

Business Problem

In this case study, we consider an e-commerce company that has accumulated historical data on customer interactions with its platform.

The goal is to:

- Predict the probability of customer churn
- Identify key factors influencing churn behavior
- Enable targeted marketing campaigns to retain high-risk customers

📂 Dataset Source

The dataset is provided in .xlsx format and contains detailed customer-level information.
🧾 Features Description
| Feature Name                | Description                                              |
| --------------------------- | -------------------------------------------------------- |
| CustomerID                  | Unique identifier for each customer                      |
| Churn                       | Target variable indicating churn (1 = Yes, 0 = No)       |
| Tenure                      | Duration of the customer’s relationship with the company |
| PreferredLoginDevice        | Customer’s preferred login device (e.g., mobile, web)    |
| CityTier                    | Classification of the customer’s city (Tier 1, 2, 3)     |
| WarehouseToHome             | Distance between warehouse and customer’s home           |
| PreferredPaymentMode        | Payment method used (credit card, debit card, COD, etc.) |
| Gender                      | Customer’s gender                                        |
| HourSpendOnApp              | Time spent on the platform (hours)                       |
| NumberOfDeviceRegistered    | Number of devices linked to the account                  |
| PreferedOrderCat            | Preferred product category in the last month             |
| SatisfactionScore           | Customer satisfaction rating                             |
| MaritalStatus               | Customer’s marital status                                |
| NumberOfAddress             | Number of saved addresses                                |
| OrderAmountHikeFromlastYear | % increase in order value from last year                 |
| CouponUsed                  | Coupons used in the last month                           |
| OrderCount                  | Number of orders placed in the last month                |
| DaySinceLastOrder           | Days since last purchase                                 |
| CashbackAmount              | Average cashback received                                |


## 🛠️ Methodology

The model development process follows a structured machine learning pipeline, integrating data preprocessing, model training, and evaluation.

### 1. Data Preprocessing

* **Missing Value Handling**: Addressed using `SimpleImputer` and `IterativeImputer` to ensure data completeness
* **Feature Encoding**: Categorical variables transformed using `OneHotEncoder`
* **Feature Scaling**: Numerical features standardized with `StandardScaler`
* **Column Transformation**: Applied `ColumnTransformer` to handle numerical and categorical features in a unified pipeline

### 2. Exploratory Data Analysis (EDA)

* Performed data exploration using **Pandas** and **NumPy**
* Visualized distributions and relationships with **Matplotlib**, **Seaborn**, and **Plotly**
* Analyzed missing data patterns using **Missingno**


### 3. Feature Selection

* Applied feature selection techniques from `sklearn.feature_selection`
* Identified the most relevant features contributing to churn prediction.

### 4. Model Development

Multiple machine learning models were implemented and compared, including:

* Logistic Regression (`LogisticRegression`, `LogisticRegressionCV`)
* Ridge Classifier (`RidgeClassifierCV`)
* Stochastic Gradient Descent (`SGDClassifier`)
* K-Nearest Neighbors (`KNeighborsClassifier`)
* Ensemble Models:

  * Random Forest (`RandomForestClassifier`)
  * Gradient Boosting (`GradientBoostingClassifier`)
  * AdaBoost (`AdaBoostClassifier`)
  * Bagging (`BaggingClassifier`)
* Extreme Gradient Boosting (`XGBClassifier`)

All models were integrated into a **scikit-learn Pipeline** to ensure reproducibility and streamline preprocessing and training.

### 5. Hyperparameter Tuning

* Used `GridSearchCV` to optimize model parameters
* Performed cross-validation to improve generalization and reduce overfitting


### 6. Model Evaluation

Models were evaluated using:

* **Accuracy Score**
* **Classification Report** (Precision, Recall, F1-score)
* **Confusion Matrix** (visualized using `ConfusionMatrixDisplay`)


### 7. Data Splitting

* Dataset divided into training and testing sets using `train_test_split`
* Ensured fair evaluation of model performance on unseen data

This approach ensures a robust and scalable pipeline, enabling reliable churn prediction and facilitating future improvements such as model deployment and real-time inference.
