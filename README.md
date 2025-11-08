🧭 Introduction

This Power BI dashboard provides an interactive and insightful view of data transformed and analyzed from multiple sources — primarily MySQL Server and MySQL Workbench. The dashboard showcases how data can be efficiently migrated, cleaned, and profiled between two different environments while maintaining data consistency and accuracy. By integrating two datasets, Product.csv and Test_Environment.csv, through SQL joins and transforming them into a unified table, the dashboard highlights key performance metrics such as sales, product performance, profit margins, and environment efficiency. Additionally, DAX functions were utilized to create dynamic measures and KPIs, enabling deeper insights into business trends and data relationships. Overall, the dashboard serves as a comprehensive visualization of the entire data transformation lifecycle — from raw CSV files to meaningful analytical insights.

## 📘 Overview
This project demonstrates an end-to-end data transformation and visualization workflow using **Power BI**, **MySQL Server**, and **MySQL Workbench**.  
The main objective of this project was to simulate a scenario where a company transitions its data source from **MySQL Server** to **MySQL Workbench**, ensuring seamless data migration, cleaning, profiling, and visualization.

Two CSV files — **Product.csv** and **Test_Environment.csv** — were imported into the SQL Server. After performing the required data transformations, the datasets were joined using SQL and then visualized in Power BI.  
Additionally, **DAX (Data Analysis Expressions)** functions were used to enhance the analytical capabilities of the dashboard and derive meaningful insights.

---

## 🗂️ Dataset
The project uses the following datasets:

1. **Product.csv** – Contains product details such as Product ID, Name, Category, and Pricing information.  
2. **Test_Environment.csv** – Contains test environment-related data such as Environment ID, Location, and Performance metrics.

After importing both files, they were combined into a single table named **`new_table`** using an SQL **LEFT JOIN** operation based on a common key (e.g., Product ID).

---

## 🧰 Tools and Technologies Used
- **MySQL Server** – Used as the initial data source for data storage and transformation.  
- **MySQL Workbench** – Used as a secondary data source after migration for profiling and transformation.  
- **Power BI** – Used for data visualization, modeling, and dashboard creation.  
- **SQL** – Used for data cleaning, transformation, and joining operations.  
- **Advanced Editor in Power BI** – Used for query modifications and connection management.  
- **DAX (Data Analysis Expressions)** – Used for calculations and dynamic measures in Power BI.

---

## 🧮 DAX Formulas Used
Below are some of the DAX measures used in this project:

```DAX
Total Sales = SUM('new_table'[Sales])

Average Price = AVERAGE('new_table'[Price])

Product Count = COUNTROWS('new_table')

Profit Margin % = DIVIDE(SUM('new_table'[Profit]), SUM('new_table'[Sales])) * 100

Sales Category = SWITCH(
    TRUE(),
    [Total Sales] <= 1000, "Low",
    [Total Sales] <= 5000, "Medium",
    [Total Sales] > 5000, "High"
)
````

---

## ⚙️ Prerequisites

To run or replicate this project, you need the following setup:

* **Power BI Desktop** (latest version)
* **MySQL Server** installed locally or on a cloud instance
* **MySQL Workbench**
* **Basic understanding of SQL queries**
* **Two CSV files:** `Product.csv` and `Test_Environment.csv`

---

## 💡 Key Insights & Analytical Questions

The dashboard aims to answer the following analytical questions:

1. What are the total sales and profit generated across all products?
2. Which product categories are performing the best?
3. What is the average price and profit margin by category or region?
4. How does performance vary between different environments?
5. Which products or environments contribute most to overall revenue?
6. Are there any noticeable patterns or outliers in product performance?
7. What is the data trend after migration from MySQL Server to MySQL Workbench?

These insights help in understanding the performance impact of switching data sources and the consistency of data across systems.

---

## 🏁 Conclusion

This project successfully demonstrates the integration of **SQL-based data sources** with **Power BI** for data cleaning, transformation, and visualization.
By combining datasets using SQL joins and enhancing reports with DAX, the project provides a strong foundation for real-world data migration and analytics tasks.
The ability to conveniently switch between **MySQL Server** and **MySQL Workbench** highlights flexibility in managing data pipelines, ensuring efficient performance and insightful visual storytelling.

---


