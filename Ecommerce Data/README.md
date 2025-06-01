# SSIS Final Project – E-Commerce Data Warehouse  
**Author:** Seema Chhunga (INT-952)  
**Technology Stack:** SQL Server, SSIS (SQL Server Integration Services), Visual Studio  

---

## 📌 Project Objective

The objective of this project is to design and implement a scalable data warehouse solution for an e-commerce business using SSIS. It covers the creation of dimensional and fact tables, implementation of ETL processes, data integrity enforcement, and error logging mechanisms.

---

## 📁 Project Contents

- `SSIS-FINAL PROJECT(ECOMMERCE DATA)-SEEMA_CHHUNGA(INT-952).sln`  
  Visual Studio solution file containing SSIS packages for ETL processes.
  
- `ssis final project (seema chhunga -INT_952).sql`  
  SQL script for setting up the entire database schema including fact and dimension tables.

---

## 🗃️ Database Schema Overview

The project adopts a star schema model comprising:

### 🔹 Dimension Tables
- **Category** – Main product categories  
- **SubCategory** – Sub-categories linked to categories  
- **Product** – Product information  
- **Supplier** – Vendor details  
- **Customer** – Customer demographics and full name  
- **MarketingCampaigns** – Promotional campaign metadata  
- **PaymentMethod** – Supported payment types  

### 🔹 Fact Tables
- **Orders** – Core transactional data  
- **OrderItem** – Line item details for each order  
- **Returns** – Returned items and refund information  

### 🔹 Supporting Tables
- **CampaignProductSubCategory** – Bridge table linking campaigns to product sub-categories  
- **CustomerProductRatings** – Customer reviews and sentiment analysis  
- **Ecommerce_ErrorLog** – Centralized error logging table for capturing ETL failures

---

## ⚙️ Implementation Details

### 🔧 ETL Process
- Built using **SSIS** in **Visual Studio**
- Integrates CSV and relational sources
- Implements data validation, transformation, and conditional loading
- Logs all data quality or load issues to `Ecommerce_ErrorLog`

### 🔐 Data Integrity
- Extensive use of `FOREIGN KEY` constraints with `ON DELETE CASCADE` and `ON UPDATE CASCADE`
- Error-handling via try/catch mechanisms and redirect rows in SSIS

---

## 🚀 Getting Started

1. Clone the repository and open the solution file in Visual Studio.
2. Execute the SQL script in SSMS to generate the schema.
3. Configure flat file and database connections in SSIS packages.
4. Run the packages to perform data extraction, transformation, and loading.

---

## 🧰 Prerequisites

- Microsoft SQL Server (2017 or later)
- SQL Server Management Studio (SSMS)
- Visual Studio 2019+ with SSIS Integration Services extension
- Required CSV source files for `Supplier`, `OrderItem`, `Returns`, etc.

---

## 🖊️ Author

**Seema Chhunga**  

Email: *seemachhunga1402@gmail.com*  


---

## 📄 License

This project is for academic and educational use only.

