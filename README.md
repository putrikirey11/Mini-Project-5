# Mini Project 5 : Improving Employee Retention by Predicting Employee Attrition Using Machine Learning
## Background
Human resources (HR) are a critical asset that needs to be effectively managed by companies to achieve business goals efficiently. In this scenario, we are faced with a human resource issue within the company. Our focus is to understand how to retain employees, as their departure can lead to increased recruitment and training costs for new hires. By identifying the key factors causing employee dissatisfaction, the company can promptly address these issues by creating relevant employee-centric programs.
## Objective
Develop a machine learning model that can predict employees who are likely to resign and provide business recommendations based on the constructed model.
## Tools
In this project, I utilized Python as the programming language, Jupyter as the notebook, and employed various libraries such as pandas, numpy, sklearn for preprocessing and machine learning, and a combination of matplotlib and seaborn for data visualization.
## Content
### Data Cleaning and Data Preprocessing
This section involves several processes such as handling missing values. Null values in the Resignation Reason feature were categorized as 'still_working' as there was no value in the Resignation Date feature, indicating that the employee had not yet resigned. The LOP Program Participation feature was dropped due to a significant number of null values. Null values in the Absenteeism Count feature were filled with 0 under the assumption that these values represented employees who had never been absent, which was supported by the absence of 0 values in the feature. Null values in the Employee Satisfaction Score, Project Participation Count, and Last Month Lateness Count features were filled with the median values of each column. Feature engineering and feature selection were performed to prepare for the model. Feature encoding was done using label encoding and One Hot Encoding. Data features and targets were split, with 70% allocated for training and 30% for testing. Feature scaling was carried out using StandardScaler. As the data was imbalanced, it was addressed using SMOTE oversampling.
### Annual Report on Employee Number Changes
![1](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/566b21d7-7ba1-4a78-9c3e-64fc373de52a)
The graph illustrates the growth in the number of employees from 2006 to 2020. It is evident that the company's situation is concerning, with a continuous decrease in the number of employees over the past four years. This could be an indication of potential internal or external issues within the company.
### Resign Reason Analysis for Employee Attrition Management Strategy
![2](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/6d8f3707-82a4-49e2-8382-db1aeb4be706)
The Data Analyst division has the highest percentage of resignations, reaching 50%.
![3](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/b8b52e55-15a7-4c35-9571-b1062b508955)
From the adjacent graph, it is apparent that all employees who resigned from the Data Analyst division were from the Fresh Graduate Program, which also had a significantly higher number of resignations compared to the number of employees who stayed.

**Recommendation:** The company can provide better self-development opportunities, such as providing training in each division, especially for new employees. Offer more competitive salary and benefits, particularly for fresh graduate program participants, and create a more supportive work environment.
![4](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/fb2d8881-d7e6-4287-80d4-ebce8d65e53e)
The graph beside it shows that out of 8 employees from the Data Analyst division who resigned, 4 had excellent performance, and 1 had good performance. This is detrimental to the company, as these resigning employees were high-performing.

**Recommendation:** The company can offer better salaries, benefits, and work-life balance to employees with good performance. Additionally, the company is expected to offer good career progression and self-development opportunities to these high-performing employees, ensuring they feel valued and have a promising career path within the company.
![5](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/2bbdcb1e-ae9c-4524-99c7-4aad3581a21d)
The graph alongside indicates that out of the various reasons for resignations, 6 employees from the Data Analyst division resigned due to toxic culture, and 2 others due to internal conflicts. Both reasons reflect some unfavorable internal factors within the Data Analyst position in this company.

**Recommendation:** The company must address internal conflicts by facilitating meetings between employees or mediators to resolve issues. Additionally, the company should reevaluate the existing organizational culture to identify what is considered "toxic" for employees and ensure that the existing culture is positive and motivating for employees!

### Data Modeling
Performed data modeling and several hyperparameter tunings. The selected model was a Decision Tree algorithm due to its superior performance compared to other models. The AUC train and test did not differ significantly, indicating that this model was not overfitting or underfitting, unlike the other models, which showed signs of overfitting. Moreover, evaluation metrics such as accuracy, precision, recall, and F1-score were also better compared to other models.

![6](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/7f408b98-e02e-47b2-a8ea-60831f529983)

## Presenting Machine Learning Products to the Business Users
![7](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/772d6001-c933-4656-bd34-4359b76b6f29)
`Length of Employment` is the most critical and dominant feature compared to other features in predicting the likelihood of an employee's resignation. The SHAP values indicate that the shorter the employment duration of an employee, the higher the probability of resignation.

![8](https://github.com/putrikirey11/Mini-Project-5/assets/131474475/03f86c60-c8dd-4da2-bfcb-50c7a310bb14)
The graph adjacent indicates a very high turnover rate among employees with 0-4 years of tenure, indicating that new employees are more likely to resign compared to long-serving employees.

## Business Recommendations
The company should focus on improving the onboarding program to ensure that new employees feel accepted and skill-ready, to avoid a toxic work environment, and reduce the high turnover rate among new employees. Provide mentorship to help them adapt to the company's environment. Foster a collaborative work culture, prioritize work-life balance, facilitate open communication, and regularly acknowledge employee contributions. Lastly, address issues promptly and fairly to create a healthy and sustainable work environment.
