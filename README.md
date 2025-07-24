# 📊 Retail Sales Analysis Using SQL

## 📁 Project Files

- **Dataset:** `retail_sales.csv`  
- **SQL Script:** `SQL_Query_Retail_Sales.sql`  
- **Tool Used:** SQL Server Management Studio (SSMS)

---

## 🎯 Project Objective

The objective of this project is to **practice SQL** by working with a retail dataset. The goal is to **clean the data, perform CRUD operations, explore the dataset**, and **extract actionable business insights**.

---

## 🧭 Project Workflow

1. **Database Setup:** Create and populate the SQL database.
2. **CRUD Operations:** Apply Create, Read, Update, Delete operations to manage data.
3. **Data Cleaning:** Ensure data consistency and remove invalid entries.
4. **Exploratory Data Analysis (EDA):** Generate questions and explore the dataset.
5. **Insights Delivery:** Extract and present key business insights.

---

## 🛠️ Database Preparation & Cleaning

### ✅ Setting up the Database

The retail data was imported into SQL Server Management Studio and formatted using the following operations:

```sql
Changing the data type from the DB
ALTER TABLE retail_sales
alter column transactions_id INT not null

ALTER TABLE  retail_sales
alter column sale_date date

ALTER Table retail_sales
alter column sale_time TIME

Alter table retail_sales
alter column customer_id INT

alter Table retail_sales
alter column gender varchar(15)

alter table retail_sales
alter column age int

alter table retail_sales
alter column category varchar(15)

alter table retail_sales
alter column quantiy INT

alter table retail_sales
alter column price_per_unit float

alter table retail_sales
alter column cogs float

alter table retail_sales
alter column total_sale float

ALTER TABLE retail_sales
add primary key (transactions_id)

-- Data Cleaning
select 
	count(*)
from retail_sales

-- Verifying if we have null's in the DB.
select *
from retail_sales
where 
	transactions_id is null
	or
	sale_date is null
	or
	sale_time is null
	or 
	gender is null
	or
	age is null
	or
	category is null
	or
	quantiy is null
	or 
	price_per_unit is null
	or
	cogs is null
	or
	total_sale is null

-- In case we have null's, we need to delete those rows.

delete from retail_sales
where 
	transactions_id is null
	or
	sale_date is null
	or
	sale_time is null
	or 
	gender is null
	or
	age is null
	or
	category is null
	or
	quantiy is null
	or 
	price_per_unit is null
	or
	cogs is null
	or
	total_sale is null
```
## Exploratory Data Analysis (EDA)

The goal of this stage is to explore trends and patterns in the dataset that can lead to actionable insights.
