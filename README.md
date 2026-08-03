# 📊 Cohort Analysis for Customer Retention

A customer retention analysis project using **Python, Pandas, and Seaborn** to understand how customer purchasing behavior changes over time through **cohort analysis**.

This project groups customers based on their **first purchase month** and measures how many customers return in subsequent months, helping businesses evaluate customer retention and lifetime engagement.

---
<img width="1057" height="534" alt="Screenshot 2026-08-03 at 3 12 54 PM" src="https://github.com/user-attachments/assets/bedf098b-ced9-4f8c-9ed2-282201594dbf" />

---

## 📌 Project Overview

Customer retention is one of the most important metrics for any business. Instead of only tracking total sales, cohort analysis allows us to answer questions such as:

- How many customers return after their first purchase?
- Which customer cohorts have the highest retention?
- How does retention change over time?
- Are newer customer cohorts performing better than older ones?

This notebook demonstrates the complete workflow of creating a cohort retention matrix from raw transactional data.

---

## 🎯 Objectives

- Clean and prepare transactional sales data
- Identify each customer's first purchase month
- Create monthly customer cohorts
- Calculate cohort indices
- Build a customer retention table
- Visualize retention trends using heatmaps

---

## 🛠️ Tech Stack

- **Python**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## 📂 Dataset

The project uses an **Online Retail** transactional dataset containing customer purchases.

Main fields used:

- CustomerID
- InvoiceDate
- Invoice Number
- Quantity
- Unit Price

---

## 🔄 Project Workflow

### 1. Import Libraries

- Pandas
- Matplotlib
- Seaborn

---

### 2. Load Dataset

- Read Excel dataset
- Inspect data structure
- Review missing values

---

### 3. Data Cleaning

- Remove transactions with missing Customer IDs
- Keep only valid customer records

---

### 4. Create Invoice Month

Extract the purchase month from each transaction.

Example:

| Invoice Date | Invoice Month |
|--------------|---------------|
| 2011-03-15 | 2011-03 |

---

### 5. Create Customer Cohorts

For every customer:

- Find their first purchase month
- Assign it as their **Cohort Month**

Example:

| Customer | First Purchase | Cohort |
|----------|----------------|--------|
| A | Jan 2011 | Jan 2011 |
| B | Mar 2011 | Mar 2011 |

---

### 6. Calculate Cohort Index

Compute the number of months since each customer's first purchase.

Example:

| Cohort Month | Purchase Month | Cohort Index |
|--------------|----------------|--------------|
| Jan | Jan | 1 |
| Jan | Feb | 2 |
| Jan | Mar | 3 |

---

### 7. Count Active Customers

Group data by:

- Cohort Month
- Cohort Index

Count the number of unique customers in each cohort period.

---

### 8. Build Cohort Table

Transform grouped data into a pivot table.

Rows represent:

- Cohort Month

Columns represent:

- Months since acquisition

Values represent:

- Unique active customers

---

### 9. Calculate Retention Rate

Normalize each cohort by dividing every month by the number of customers in Month 1.

Formula:

Retention Rate = Active Customers / Initial Customers

---

### 10. Visualize Results

Generate two heatmaps:

- Customer Count Heatmap
- Customer Retention (%) Heatmap

These visualizations make it easy to identify strong and weak customer retention patterns.

---

## 📈 Key Insights

The analysis helps answer questions like:

- Which acquisition months retain customers the best?
- How quickly do customers churn?
- What percentage of customers return after 2, 3, or 6 months?
- Which cohorts show long-term loyalty?

---

## 📷 Output

The notebook produces:

- Customer Cohort Table
- Retention Matrix
- Customer Count Heatmap
- Retention Percentage Heatmap

---

## 🚀 Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Customer Analytics
- Cohort Analysis
- Customer Retention Analysis
- Data Visualization
- Business Intelligence
- Pandas Data Manipulation
- Heatmap Visualization

---

## 💼 Resume Highlights

- Performed customer cohort analysis on transactional retail data using Python and Pandas.
- Built customer retention matrices by grouping users based on acquisition month.
- Calculated cohort indices and monthly retention rates to measure repeat customer behavior.
- Created heatmap visualizations using Seaborn to identify retention trends and customer lifecycle patterns.
- Applied data cleaning, feature engineering, grouping, pivot tables, and business analytics techniques to generate actionable insights.

---

## ⭐ Future Improvements

- Revenue-based cohort analysis
- Customer Lifetime Value (CLV)
- RFM Segmentation
- Repeat Purchase Rate analysis
- Interactive dashboard using Tableau or Power BI
- Retention forecasting

---

## 👤 Author

**Suyog Yadav**

If you found this project useful, feel free to ⭐ star the repository.
