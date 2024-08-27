# Customer-Churn-Retention
Pwc Power BI Virtual Work - Task 2

### **Problem Statement :** 
The purpose of this task is to -
* Define proper KPI's
* Create a dashboard for the retention manager reflecting the KPI's
* Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed
* Customers who left within the last month
* Services each customer has signed up for: phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
* Customer account information: how long as a customer, contract, payment method, paperless billing, monthly charges, total charges and number of tickets opened in the categories administrative and technical
* Demographic info about customers – gender, age range, and if they have partners and dependents

### **Datasource :**
Dataset used for this task was presented by Pwc.
* Dataset: Customer Churn Retention

### **Data Analysis (DAX):**
Measures used in all visualisation are:

* Average MonthlyCharges = AVERAGE('01 Churn-Dataset'[MonthlyCharges])

* Average TotalCharges = AVERAGE('01 Churn-Dataset'[TotalCharges])

* churn count = CALCULATE(COUNT('01 Churn-Dataset'[Churn]), ALLSELECTED('01 Churn-Dataset'[Churn]),'01 Churn-Dataset'[Churn] = "Yes")

* churn rate % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Churn]), '01 Churn-Dataset'[Churn] = "yes" ), COUNT('01 Churn-Dataset'[Churn]), 0)

* Dependent in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]), '01 Churn-Dataset'[Dependents]="Yes",'01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Churn]="Yes"), 0)

* Device protection in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]), '01 Churn-Dataset'[DeviceProtection] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[DeviceProtection]),'01 Churn-Dataset'[Churn]="Yes"),0)

* Online backup in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]), '01 Churn-Dataset'[OnlineBackup] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)

* Online security in % =DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]), '01 Churn-Dataset'[OnlineSecurity] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)

* Partner in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Partner]="Yes",'01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[Partner]), '01 Churn-Dataset'[Churn]="Yes"), 0)

* Phone service in % =DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]), '01 Churn-Dataset'[PhoneService] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0)

* SeniorCitizen in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[SeniorCitizen]=1,'01 Churn-Dataset'[Churn]="Yes"), CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn]="Yes"), 0)

* Streaming Movies in % =DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]), '01 Churn-Dataset'[StreamingMovies] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0)

* Streaming TV in % =DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]), '01 Churn-Dataset'[StreamingTV] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)

* Tech Support in % =DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]), '01 Churn-Dataset'[TechSupport] ="Yes", '01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[TechSupport]),'01 Churn-Dataset'[Churn]="Yes"),0)

### **Insights:**
As shown the data Visualisation, It can be deduced that:

* Customers on the Two-Year contract have been with the company for long, while most of the customers on Month-to-Month contract joined the company.
* The company is at risk of losing recently joined customers. based on the results from analysis.. if they decided to month-to-month contract.
* 7043 customers are at the risk of churn. and The churn rate is 27% and yearly charges are $16.06M charges. and Monthly Charges are $456.12K monthly charges.
* 2955 tech tickets were opened and 3632 admin tickets were opened.
* Most of the churned customers did not sign up for Online Security and tech support and also did not sign up for Phone Services.
* A lot of customers had an issue with Fiber Optic . Up to 42% of the customers churned were using Fiber Optic as their Internet Services.
### **Recommendation:**
* The Company could try convincing customers to subscribe to One-Year and Two-Year contracts. The contracts are not favourable to customers as they tend to pay more monthly.
* Giving the discount to customers based on some specific tasks is also good at retaining them, specially those month-to-month contracts.
* From analysis majority customers who churned did not sign up for Online Security and Tech Support. These are the important services that customers should sign up for. The company should educate customers on the * benefits of signing up for these services.
* Increase sale of 1 and 2 year contracts by 5% each and Yearly increase of automatic payments by 5%.
