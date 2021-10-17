# Atliq-hardware-sales-Insights



Purpose:
To unlock sale insights that are not visible before sales team for decision. Support and automate them to reduced manual time spend in data gatherings.
Mysql database has all sales transactions, customers, products and markets information. I have analyse this database and then hook it up with power BI. In power BI I have performed ETL and data cleaning operations to build our dashboard. 

Problem Statement:
Atliq Hardware supplies hardware and peripherals to many hardware store clients. They have head office in Delhi and many regional offices. Their sales are fluctuating rapidly and the Sales Director is having issue to keep insights and track of the growth or decline as there are so many excel files merged to form an SQL database.

Stakeholders:
•	Sales Director
•	IT Team
•	Data Analytics Team
•	Marketing Team
•	Customer Service Team

Success Criteria:
•	Sales Insights and trends are available to the Sales Director and teams to provide Data Driven Decisions.
•	Automated Procedure to save time taken manually


 
 Steps followed:
1) ETL (Extract, Transform, Load)
•	Extracted Data from MySQL database to Power BI
•	Transformed Data Using Power Query
•	Loaded transformed data into Power BI

2) Build a Dashboard
•	Build a proper dashboard that will help the user to get useful insights from the records

3) Feedback on Dashboard from User
•	As the stakeholders to use the Dashboard and provide feedback on what should be improved



Data Analysis using SQL
1.	Show all customer records
SELECT * FROM customers;

2.	Show total number of customers
SELECT count(*) FROM customers;

3.	Show transactions for Chennai market (market code for Chennai is Mark001
SELECT * FROM transactions where market_code='Mark001';

4.	Show distrinct product codes that were sold in chennai
SELECT distinct product_code FROM transactions where market_code='Mark001';

5.	Show transactions where currency is US dollars
SELECT * from transactions where currency="USD"

6.	Show transactions in 2020 join by date table
SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7.	Show total revenue in year 2020,
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8.	Show total revenue in year 2020, January Month,
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9.	Show total revenue in year 2020 in Chennai
SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

![Atliq Hardware Sales Insights](https://user-images.githubusercontent.com/85544024/125155125-a4634f00-e17f-11eb-9455-3f4225edfc70.png)

![Atliq Hardware Sales Insights 1](https://user-images.githubusercontent.com/85544024/125155137-af1de400-e17f-11eb-8f4a-bfca719a5345.png)

![Atliq Hardware Sales Insights 2](https://user-images.githubusercontent.com/85544024/125155132-a9280300-e17f-11eb-8e75-7302de0a9236.png)














