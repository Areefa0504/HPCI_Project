# High Performance Computational Infrastructures
This is a project using Mapreduce 

Introduction:
===============
Comcast Corporation Pvt Ltd (imaginary) is a Telecommunication organization that provides telecommunication services to millions of customers. Typically, a single customer can generate a significant amount of data, including internet usage, TV viewing habits, and customer churn rate which requires advanced data processing and highperformance computational infrastructure capabilities to manage and make sense of the collected data. To analyze sales transactions, Comcast Telecommunication uses an advanced data analytics system that utilizes Hadoop and machine learning algorithms. The system can identify patterns in customer behavior, such as it provides insights into which customers are likely to churn, enabling the company to take proactive measures to retain them. Due to the vast amount of data being generated every day, Comcast uses the Hadoop system, and cloud storage to store the data. The company employs a robust security system to ensure the privacy and security of the data.

1.2 Problem Description:
==========================
The biggest problem of the telecommunication organization today is that customers discontinue using the company’s services. When customers cancel their subscriptions, the 
company loses revenue, and it becomes more expensive to acquire new customers. High customer churn rates can lead to reduced revenue, increased customer acquisition cost, 
and damage to a company’s reputation. To understand the factors that contribute to customer churn, the telecommunication industry has decided to do research on the below 
question.

Research Question:
====================
1. “Are the customers canceling/leaving the subscription when they subscribe smaller contract period (Month-to-Month) and how does it vary from people having dependents?”

The question being asked is whether customers are more likely to cancel or leave their subscriptions when they choose smaller contract periods, such as month-to-month, and 
whether this varies for customers with dependents. This research question is crucial as it can provide valuable insights into customer behavior and enable the industry to take proactive measures to reduce customer churn and improve customer retention. Customer satisfaction is a key component of any industry, and understanding whether 
customers are more likely to cancel their subscriptions when they opt for smaller contract periods can help the telecommunication industry develop targeted retention strategies. For example, they could offer incentives to customers who sign up for longer contract periods or create customized plans that cater to the needs of customers with dependents. By implementing such strategies, the industry can improve customer satisfaction and decrease churn rates. This research question requires the expertise of a senior data scientist who can analyze customer data to identify patterns and trends. The data engineering team also plays a crucial role in the process as they are responsible for managing the data infrastructure and ensuring that the data is accurate and reliable. Additionally, the marketing team may be involved in creating retention strategies based on the findings of the research.

Associated Dataset:
=====================
The dataset for this analysis was obtained from Kaggle.com and can be found at the following URL, [https://www.kaggle.com/blastchar/telco-customer-churn](url). The dataset 
contains a total of 21 columns and 7,043 rows. The size of the dataset is around 955KB. It has information about customer demographics such as age, gender, dependency, and 
usage patterns, and account information such as the type of plan and the contract period along with whether each customer churned or remained with the company. The complete 
data dictionary is mentioned below in the table.

Data Description:
======================
customerID: Customer identification Number
gender: Whether the customer is a male or a female	
SeniorCitizen:	Whether the customer is a senior citizen or not	
Partner:	Whether the customer has a partner or not	
Dependents:	Whether the customer has dependents or not	
tenure:	Number of months the customer has stayed with the company	
PhoneService:	Whether the customer has a phone service or not	
MultipleLines:	Whether the customer has multiple lines or not	
InternetService:	Customer’s internet service provider	
OnlineSecurity: Whether the customer has online security or not	
OnlineBackup:	Whether the customer has online backup or not	
DeviceProtection:	Whether the customer has device protection or not	
TechSupport:	Whether the customer has tech support or not	
StreamingTV:	Whether the customer has streaming TV or not	
StreamingMovies:	Whether the customer has streaming movies or not	
Contract:	The contract term of the customer	
PaperlessBilling:	Whether the customer has paperless billing or not	
PaymentMethod:	The customer’s payment method
MonthlyCharges:	The amount charged to the customer monthly	
TotalCharges:	The total amount charged to the customer	
Churn:	Whether the customer churned or not

Design and Implementation:
========================
To answer the question, the data in the customer churn CSV file must be filtered to get contract, dependents, and churn information of all customers and then the logic to find out the number of customers churned based on contract and how it varies from people having dependents. So, I used a single MapReduce Job to achieve this. First data will be passed through the mapper class (ChurnMapper) to get the fields required to filter out from customer information. After that, a reducer class (ChurnReducer) takes the output of the mapper class and then the business logic is applied on it. A driver class (ChurnAnalysis) is implemented to run the whole project(.jar).

For complete implementation and design please use the file 







