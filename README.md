# Employee Attrition Prediction

## Business Understanding
*	Problem : Company 'X' has a 36.4 percent employee attrition rate, while the usual attrition rate is 10.9 percent. This is not good because a high attrition rate implies more resources for hiring and training new employees. Furthermore, it will increase the workload of the remaining workers and cause many projects to also be delayed.
*	Goals : Reducing employee attrition at Company 'X'.
*	Objective : Understanding the factors that most influence attrition rates in this company and make recommendations on what companies can do to reduce attrition rates.
*	Business Metrics : Attrition rate

## Data Understanding
The dataset contains information from 1470 employees. The information consists of employee attrition, employee profile, employee performance, and employee status. Details of the data features are age, daily rate, distance from home, education, employee count, employee number, environment satisfaction, hourly rate, job involvement, job level, job satisfaction, monthly income, monthly rate, number companies worked, percent salary hike, performance rating, relationship satisfaction, standard hours, stock option level, total working years, training times last year, work life balance, years at company, years in current role, years since last promotion, years with current manager, attrition, business travel, department, education field, gender, job role, marital status, over 18, over time.

Data source : https://www.kaggle.com/patelprashant/employee-attrition

## Data Insights
*	Over Time has the highest positive correlation with attrition, while Total Working Years has the lowest negative correlation, and Business Travel has almost no correlation with attrition.
*	Overtime employees have a higher rate of attrition than non-overtime employees, according to the Over Time feature.
*	The Laboratory Technician role has the highest attrition percentage in the Job Role feature, while the Research Director role has the lowest.
*	Job level 1 has the highest attrition percentage in Job Level features, while job levels 4 and 5 have the lowest attrition percentage.
*	The percentage of attrition in married employees is higher than in married and divorced employees, as shown in the Marital Status feature. Employees who are divorced have the lowest percentage of attrition.
*	In the Department feature, the highest to lowest attrition percentages are Research & Development, Sales, and Human Resources.
*	According to the Gender feature, male employees have a higher rate of attrition than female employees.
*	In the Monthly Income feature, the higher the monthly income, the lower the employee attrition percentage.
*	In the Years In Current Role feature, the longer the employee is in the current role, the lower the employee attrition percentage.
*	In the Years Since Last Promotion feature, the highest percentage of employee attrition is 0 years.
*	In the Number Companies Worked feature, the highest percentage of employee attrition is for employees with a number of companies worked of 2 and the lowest percentage is for employees with a number of companies worked of 8.
*	Employees with Education Field life science have the highest attrition rate, while employees with human resources education have the lowest attrition percentage.
*	Employees with a Distance From Home of 1 - 5 have the highest attrition rate, whereas employees with a distance from home of > 25 have the lowest attrition rate.

## Data Preparation
* Handle outlier by transforming values and imputation
* Feature encoding
* Removed unused features

## Modeling
* The features that will be used are standardized and oversampled before they are modeled (because the features are imbalanced).
*	The algorithms used to build the predictive model of employee attrition in company 'X' are Logistic Regression, K-Nearest Neighbors Classifier, Decision Tree Classifier, Random Forest Classifier, XG Boost Classifier, dan Ada Boost Classifier.
*	The metrics used to evaluate the model are Accuracy, Precision, Recall, and F-1 Score.
*	Because we don't want a large False Negative rate (prediction: retain, actual: attrition), the best algorithm is chosen based on the highest value of the Recall metric.

## Model Insights
*	According to the model evaluation results, the Logistics Regression model with a Recall-Score of 0.83 is the best classification model for predicting attrition.
*	The results of the Logistic Regression model hyperparameter tuning were not different from the results before the hyperparameter tuning. This may be due to the small size of the dataset, possibly cause the results to be insignificant.
*	Overtime is the most influential feature on attrition, followed by years since last promotion, marital status, number of companies worked for, and department. Monthly income has the least of an impact on attrition.

## Business Recommendation
Because over time is the most influential factor on employee attrition at Company X, handling over time is a logical step that the company can take to reduce employee attrition. Simulation can be used to determine whether or not handling over time can reduce attrition. Here, the simulation that will be carried out is to reduce the level of employee over time up to 20%. The simulation will be applied to 20% of employees in this company. Before to the simulation, the employee attrition rate was 28.6 percent, and after the simulation was implemented, it was 25.9 percent.

