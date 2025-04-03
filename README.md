# RFM-Analysis
This project conducts an RFM (Recency, Frequency, Monetary) analysis to assess customer retention levels. The analysis is based on an e-commerce dataset sourced from Kaggle. By applying RFM segmentation, we can identify customer behavior patterns and generate valuable insights to support business decision-making.

# Dataset
The dataset used for this analysis contains the following columns:
- InvoiceNo: Invoice number.
- StockCode: Product identifier.
- Description: Product description.
- Quantity: Quantity of the product purchased.
- InvoiceDate: Date of the transaction.
- UnitPrice: Price per unit of the product.
- CustomerID: Unique identifier for the customer.
- Country: Country of the customer.

# Data Preprocessing

Before performing RFM analysis, the following steps were taken:
- Converted the InvoiceDate column to datetime format.
- Addressed negative values and outliers in the UnitPrice and Quantity columns.
- Removed duplicate records.
- Filled null values in the StockCode column using the mode.
- Dropped rows with null values in the CustomerID column.
- Added additional time-related features like MonthYear, yearmonth, year, month, quarter.
- Added Revenue column by multiplying UnitPrice and Quantity to reflect the total revenue per transaction
- Addressed outliers in Revenue column.

# RFM Analysis
Steps Taken:
1.	RFM Metric Calculation:
- Recency: The number of days since the last transaction for each customer.
- Frequency: The total number of transactions made by each customer.
- Monetary: The total spending of each customer.
2.	Segmentation:

    Based on the RFM scores, customers were segmented into the following categories:
- Highly Retained: Highest scores (555, 545, etc.), indicating strong loyalty and frequent purchases.
- Retained Customer: High Recency and Frequency, meaning they are still actively shopping.
- At Risk: Mid-range scores, indicating customers who are decreasing in engagement.
- Churned Customer: Low scores, representing customers who have stopped purchasing.
- Average Customer: Customers with inconsistent shopping patterns that do not strongly fit other categories.

# Key Insights:
- The "Highly Retained" segment is minimal, indicating that only a small fraction of customers make frequent transaction with high transaction values.
- A significant number of customers fall into the "At Risk" and "Churned Customer" segments, meaning many have reduced purchase frequency or have stopped buying altogether.
- Most customers belong to the "Average Customer" segment, showing irregular purchasing behavior and weak brand loyalty.

# Tools:
- Python
- Pandas
- Numpy
- Maplotlib
- Seaborn



