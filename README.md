## Sales Insights Data Analysis Project

 
##Problem statement of Sales insight Project:

##Objective:

 1.A company that supplies computer hardware and peripherals to many clients across India.
2.The sales director is facing a lot of challenges. The marketing is growing dynamically, he is struggling to keep track of the sales. He needs more accurate 	insights about the company sales and then makes the necessary decisions.
 
 ##Solution:
 
 Its cover project planning and data discovery aspect of our sales insights data analysis project. Once sales directory of atliQ hardware(one of the company) 	     has decided to invest in data analysis project they will do a meeting with IT director, data analytics team to come up with a plan. 
 
##Ideas:

1.Create a simple and informative dashboard about the company sales.

2.I used SQL queries in MySQL Workbench to look into the data and Power BI for ETL and Visualizations to create the insights dashboard.


### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


Data Analysis Using Power BI
============================

##Here with I have attached my dashboard image:

![image](https://user-images.githubusercontent.com/118765347/218852616-c949e554-d329-43ff-8a69-3094cb5da94c.png)

#Coclusion:

A dashboard is used for presenting a real-time status of business, monitoring business performance in

organizations. An effective dashboard is able to facilitate decision-making process and to quickly trigger actions

by delivering information to end users. In this project, a sales department, facing a large amount of data every

day, requires a visual communication from data to information. To achieve a better data visualization,

Microsoft power BI is integrated to visualize and display sales data through dashboard
