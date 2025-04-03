### Bank Customer Churn Analysis - EDA, Predictive Modelling, Evaluation
---

###1. Project Overview
 -This project  performs an exploratory data analysis (EDA) , predictive modeling by using 3 training models and result evaluation on a dataset related to customer churn . 
 -**Libraries Imported**
 -Pandas, NumPy (for data handling).
 -Seaborn, Matplotlib (for visualization).
 -Scikit-learn (for preprocessing, model training, evaluation)


---


###2. Dataset Overview
 -18 columns, including customer demographics, credit scores, balance, tenure, product ownership, and satisfaction scores.
 -Features like Credit Score, Age, Balance, NumOfProducts, IsActiveMember, and Estimated Salary are analyzed.


---

###3. Steps and Workflow
  1. Data Cleaning
  - **Handle irrelevant columns **: `Row number`, `Customer`, and `Surname` 
  - **Fix data types**: dtypes seems to be consistent

  2. EDA (Exploratory Data Analysis)
   - **Correlation Matrix**: 
   - Features impacting churn rate in positive direction is **balance, age, complaint**.
   - **Member status, number of products and credit score** are negatively correlated with exited
   - **Exited & Complain** have **100%** correlation .

  3.**Churn as Target Variable**:
   - Analyzed **churn  by Gender, Geography, Age group, Number of products, credit card, Member status, Tenure**.
  
  4. **Continuous Variables**:
   - Used **Distribution curves** to show correlations among `credit score`, `Estimated Salary`.

---

###4. Data Preprocessing
  - **label Encoding**: Converting categorical columns `Gender`, `Geography` to numeric.
  - **Balancing Data**:Resampling the data using SMOTE.
  - **Correlation**: To detect correlation between features after resampling.

 1. Test Splitting the Data
  - **Feature Scaling**: StandardScaler used for feature scaling  

---

### 5. Model prediction and Evaluation
  - **Logistic Regression, Decision Tree Classifier, Random Forest Classifier**
  -**Predictions** accuracy, precision, ROC AUC 
  - **Plotting ROC curve** for all three models
  - **Sample data is trained with all three models for comparison 

---

###6. Insights
 -The correlation matrix has an interesting relationship- **the complaint and Exited variables are 100% positively correlated**.
 -Churn Rate- **about 20% of customers are leaving the bank, out of the 10,000.**
 -Churn vs. Features
 -Gender: **25.07% of female customers vis-a-vis 16.47% male customers are exiting.**
 -Geography: Amongst the countries, **Germany has the highest churn rate of 32.44%, followed by Spain (16.67%) and France (16.17%)**.
 -Age Group: The majority of customers leaving are in the **50-60 age range, with a churn rate of 56.21%, followed by the 40-50 age group with a corresponding rate of 33.96%**.
 -Tenure : Even loyal customers with ten years of association have a churn rate of 20%. Customers below the one year mark have a churn rate of 23%.
 -Active Member: Non-active members have a higher churn rate of 27% while active customers of the bank have a churn of 14%.
 -Number of Products: Interestingly, customers with higher number of products are more likely to churn. Customers who have bought 3 products have a churn rate of 83% while those who bought        only one product have a churn rate of 28%.
 -For the continuous variables of Credit Score, Balance &Estimated Salary the following was observed-
 -The mean Credit score is about 650.The variable has an almost Gaussian Distribution.
 -A normal distribution is also seen for the balance variable. However, a little over 3,500 customers have zero balance in their accounts. This is a significant outlier for a total of  10,000 clients.
 -The Estimated Salary follows the uniform distribution.
 -All three models show **same output** for sample input data and show similar ROC value.
 -**ROC AUC** value is high for **Random Forest model(0.93) and lowest Logistic Regression (0.80)**.
 -Accuracy of Models
   -**Logistic Regression - 67%**.
   -**Decision Tree Classifier - 80%**.
   -**Random Forest Classifier- 85%**.

---

###7. Future Work
- **Feature Scaling **: 
   - Further can look for another feature scaling to evaluate the accuracy
- **Test Trail Split**:  
   - Can use 75-25 ratio
- **Model predicting**:
   -Other models for training **KNeighborsClassifier, GradientBoositngClassifier** can be used  
 -**Grid Searching**:
   -Use Grid searching for evaluating the hyperparameters of the models

---


###8. Conclusion
This project offers valuable insights into the Bank Customer Churn, helping bank to understand why customers are churned . By using **EDA techniques, Predictive Modelling**, we identified key trends and developed actionable recommendations. Future improvements can involve advanced analytics and including more predictive modeling to further enhance the findings.

---
