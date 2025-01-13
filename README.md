# RFM-Analysis

This repository contains a detailed analysis of an e-commerce dataset from the UK, sourced from Kaggle, with a focus on Recency, Frequency, and Monetary (RFM) analysis. The dataset consists of transactional data from an online retail store. This project aims to segment customers based on their purchasing behavior to provide actionable insights for business strategy.

#Project Overview

The goal of this analysis is to segment customers based on three key metrics:

•	Recency: How recently a customer made a purchase.

•	Frequency: How often a customer makes a purchase.

•	Monetary: How much a customer spends in total.

RFM analysis helps business identify high-value customers, and it provides insight into customers behaviour, enabling business to tailor marketing strategies and improve customer retention.

# Dataset
The dataset used for this analysis can be found in kaggle. It contains the following columns:

•	InvoiceNo: Invoice number.

•	StockCode: Product identifier.

•	Description: Product description.

•	Quantity: Quantity of the product purchased.

•	InvoiceDate: Date of the transaction.

•	UnitPrice: Price per unit of the product.

•	CustomerID: Unique identifier for the customer.

•	Country: Country of the customer.

# Data Preprocessing

Before performing RFM analysis, the following steps were taken:

•	Handling Missing Data: Null values in the Description column were filled using the most frequent description for each StockCode, and rows with missing descriptions were dropped.

•	Date Transformation: The InvoiceDate column was converted to a datetime format, and additional time-related features like MonthYear, hour, and dayofweek were added.

•	Revenue Calculation: A new column, Revenue, was created by multiplying UnitPrice and Quantity to reflect the total revenue per transaction.

# RFM Analysis

Steps Taken:

1.	RFM Metric Calculation:

•	Recency: The number of days since the last transaction for each customer.

•	Frequency: The total number of transactions made by each customer.

•	Monetary: The total spending of each customer.

2.	Segmentation:

Based on the RFM scores, customers were segmented into the following categories:

•	Top Customers: Customers with the highest RFM scores.

•	High Value Customers: Customers with high frequency and monetary values.

•	Medium Value Customers: Customers with moderate RFM scores.

•	Low Value Customers: Customers with low RFM scores.

•	Lost Customers: Customers who have not made a purchase recently.

#RFM Scoring:

Each customer is assigned an RFM score based on their Recency (R), Frequency (F), and Monetary (M) scores. These scores are then used to categorize customers into different segments for better targeting and personalized marketing strategies.
Segmentation Strategy:
The RFM scores were used to divide customers into 5 segments:

•	Top Customers: The top 20% of customers with the highest RFM scores.

•	High Value Customers: Customers with moderately high scores.

•	Medium Value Customers: Customers with average RFM scores.

•	Low Value Customers: Customers with low RFM scores.

•	Lost Customers: Customers who have not made a recent purchase or are not likely to make future purchases.


