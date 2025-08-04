# Employee_performance_retention_prediction_analysis

# Libraries Installed and Imported
TensorFlow is installed for deep learning. Libraries like pandas, numpy, matplotlib, seaborn, sklearn, and tensorflow.keras are imported for: Data manipulation, Visualization, Modeling (classification & regression), Evaluation (accuracy, precision, recall, F1, MSE, R²).

# 1. Project Objective
The main goal of the project was to understand and predict employee behavior using company data. Specifically, it aimed to:

- Predict whether an employee would leave the organization (attrition prediction – a classification task)

- Predict the employee’s performance score (a regression task)
This helps HR teams to take proactive actions to retain employees and improve workplace performance.

# 2. Data Understanding & Cleaning
The dataset was loaded from a CSV file named employee_data.csv.

It contained columns like EmployeeID, Age, Department, Salary, YearsAtCompany, PerformanceScore, and Attrition.

Checked for duplicate records using the EmployeeID column to ensure data quality.

Used functions like .info() and .describe() to understand data types, spot missing values, and get statistical summaries (mean, min, max, etc.).

No missing values or duplicate entries were found, which meant the dataset was clean and ready for analysis.

# 3. Exploratory Data Analysis (EDA)
Created pair plots to see how features like Age, Salary, and Years at Company were related to Attrition.

Plotted a heatmap of correlations to find which features were strongly related. For example, Salary and PerformanceScore had a positive correlation.

Used boxplots to check for extreme values or outliers in numeric columns. This helps prevent skewed model results.

Overall, this step helped build an understanding of what features might influence attrition or performance.

# 4. Data Preprocessing
Categorical variables such as Attrition (Yes/No) and Department (e.g., HR, Sales, IT) were converted into numbers using label encoding so that machine learning models could use them.

Numeric columns like Age, Salary, and YearsAtCompany were standardized using scaling. This ensures that all features are on a similar range, which helps models like neural networks train better.

The dataset was then split into training and testing sets for both classification and regression tasks.

# 5. Model Building
## A. Classification Model – Predicting Attrition
Built a Random Forest Classifier to predict whether an employee would leave or not.

Also created a deep learning model using Keras with a sigmoid output layer for binary classification.

The models were trained on employee data (e.g., Age, Salary, Department, Performance Score) and tested on unseen data.

Performance was evaluated using metrics like:

Accuracy – How many predictions were correct overall

Precision – Out of all employees predicted to leave, how many actually left

Recall – Out of all employees who actually left, how many were correctly predicted

F1-Score – A balance between precision and recall

### B. Regression Model – Predicting Performance Score
Built a Linear Regression model to predict the numeric PerformanceScore.

Also built a deep learning regression model using ReLU activations and MSE loss.

These models learned to estimate performance based on features like Age, Salary, and Years at the Company.

Model quality was measured using:

R² Score – How much of the variation in performance is explained by the model

Mean Squared Error (MSE) – How far the predictions are from actual values, on average

# 6. Statistical Analysis
Calculated attrition probability by department to find which departments had more people leaving.

Used Bayes’ theorem to calculate conditional probability – for example, how likely someone is to leave if they have a low performance score.

Performed an ANOVA test (Analysis of Variance) to see if performance scores were significantly different across departments.

The p-value from ANOVA was less than 0.05, which means department does affect performance significantly.

# 7. Key Insights
Employees with low performance scores are more likely to leave, based on both statistical and machine learning results.

Some departments have higher attrition rates than others.

Performance score is influenced by department, as confirmed by the ANOVA test.

Both traditional models (Random Forest, Linear Regression) and deep learning models gave good results, showing flexibility in approach.

Classification metrics (precision, recall, F1-score) provided deeper insight than accuracy alone.

# 8. Conclusion
This project successfully combined data cleaning, exploratory analysis, statistics, machine learning, and deep learning to understand employee behavior. It showed that factors like performance, department, and salary are important in predicting attrition and performance. The use of both classification and regression models provided a complete picture, and evaluation metrics confirmed the reliability of the results. Such an analysis can help companies make informed decisions about talent management, retention strategies, and performance improvement initiatives.
