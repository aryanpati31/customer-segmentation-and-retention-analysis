# Customer Segmentation and Retention Analysis

Customer segmentation and retention analysis using RFM analysis, cohort analysis, and K-Means clustering.

---

## Project Overview

This project analyzes customer purchasing behavior using transactional data to understand customer value, purchasing patterns, and customer retention.

The analysis combines exploratory data analysis, cohort retention analysis, RFM analysis, and K-Means clustering to identify meaningful customer segments and generate actionable business insights.

---

## Business Objectives

- Analyze customer purchasing behavior.
- Identify repeat and one-time customers.
- Analyze monthly revenue and customer activity trends.
- Evaluate customer retention using cohort analysis.
- Segment customers based on Recency, Frequency, and Monetary value.
- Identify high-value and at-risk customer segments.
- Provide data-driven recommendations for customer retention and revenue growth.

---

## Dataset

The dataset contains transactional customer purchase data, including:

- Invoice Number
- Product Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

After data cleaning, the analysis included **392,692 valid transaction records** from **4,338 unique customers**.

---

## Key Analysis Performed

### 1. Data Cleaning and Feature Engineering

The following steps were performed:

- Removed records with missing Customer IDs.
- Removed cancelled transactions and invalid purchases.
- Removed transactions with non-positive quantities or prices.
- Created a `TotalAmount` feature.

### 2. Customer Behaviour Analysis

Key business metrics calculated:

- **Total Customers:** 4,338
- **Total Revenue:** 8.89 Million
- **Total Orders:** 18,532
- **Average Order Value:** 479.56
- **Repeat Customer Percentage:** 65.58%

### 3. Monthly Sales and Customer Activity Analysis

The project analyzes:

- Monthly revenue trends
- Monthly active customers
- Monthly repeat customers

### 4. Cohort Retention Analysis

Customer cohorts were created based on the month of their first purchase.

A cohort retention heatmap was used to analyze how customer retention changes over time.

### 5. RFM Analysis

Customers were evaluated using:

- **Recency** – Days since the customer's most recent purchase
- **Frequency** – Number of unique orders placed
- **Monetary** – Total amount spent by the customer

### 6. Customer Segmentation Using K-Means

RFM features were transformed and standardized before applying K-Means clustering.

The Elbow Method was used to select **3 customer clusters**.

The identified segments were:

| Customer Segment | Number of Customers | Key Characteristics |
|---|---:|---|
| High-Value Loyal Customers | 1,320 | High frequency and spending, recently active |
| Inactive / At-Risk Customers | 981 | Long time since purchase, low frequency and spending |
| Regular Low-Value Customers | 2,037 | Relatively low spending and purchase frequency |

---

## Key Findings

- The analysis included **4,338 customers** and generated approximately **8.89 million in total revenue**.
- **65.58% of customers were repeat customers**.
- High-Value Loyal Customers represented approximately **30% of customers** but generated **81.57% of total revenue**.
- Inactive / At-Risk Customers had the highest average recency and low purchase frequency.
- Regular Low-Value Customers represented the largest customer segment and provide an opportunity for increasing customer value.
- Customer value was highly unevenly distributed, highlighting the importance of targeted customer strategies.

---

## Business Recommendations

- Protect High-Value Loyal Customers through personalized rewards and loyalty programs.
- Use targeted win-back campaigns to reactivate Inactive / At-Risk Customers.
- Increase engagement and spending among Regular Low-Value Customers through cross-selling and targeted promotions.
- Monitor cohort retention patterns to identify periods of declining customer engagement.
- Use segment-specific marketing strategies rather than applying the same approach to all customers.

---

## Visualizations

The project includes:

- Monthly Revenue Trend
- Monthly Active Customers
- Monthly Repeat Customers
- Customer Cohort Retention Heatmap
- RFM Distributions
- Elbow Method for K-Means Clustering
- Customer Segment Distribution
- Segment-Level RFM Comparison
- Revenue Contribution by Customer Segment
- Customer Segment Scatter Plots
- Normalized Customer Segment Profile Heatmap

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Project Structure

```text
customer-segmentation-and-retention-analysis/
│
├── customer_segmentation_and_retention_analysis.ipynb
└── README.md
