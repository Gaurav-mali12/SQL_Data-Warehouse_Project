# Gold Layer Data Catalog

## Overview
The Gold Layer represents the finalized, business-consumable data layer designed for reporting, dashboards, and analytical workloads. It is structured using dimension tables and fact tables that store descriptive attributes and measurable business events.

---

## 1. gold.dim_customers

### Description
This dimension table contains customer information enriched with personal, demographic, and geographic attributes to support customer-level analysis and reporting.

### Columns

| Column Name     | Data Type    | Description |
|-----------------|-------------|-------------|
| customer_key    | INT         | Surrogate key that uniquely identifies each customer record within the dimension table. |
| customer_id     | INT         | Unique numeric identifier assigned to the customer in the source system. |
| customer_number | NVARCHAR(50)| Alphanumeric customer reference code used for identification and tracking purposes. |
| first_name      | NVARCHAR(50)| Customer’s first or given name as recorded in the system. |
| last_name       | NVARCHAR(50)| Customer’s last name or family name. |
| country         | NVARCHAR(50)| Country of residence of the customer (e.g., Australia). |
| marital_status  | NVARCHAR(50)| Marital status of the customer such as Single or Married. |
| gender          | NVARCHAR(50)| Gender of the customer (Male, Female, or n/a). |
| birthdate       | DATE        | Date of birth of the customer stored in YYYY-MM-DD format. |
| create_date     | DATE        | Date when the customer record was created in the system. |

---

## 2. gold.dim_products

### Description
This dimension table stores detailed product information along with classification, pricing, and operational attributes used for product analysis.

### Columns

| Column Name          | Data Type    | Description |
|----------------------|-------------|-------------|
| product_key          | INT         | Surrogate key uniquely identifying each product record in the dimension table. |
| product_id           | INT         | Internal numeric identifier used to reference the product. |
| product_number       | NVARCHAR(50)| Structured alphanumeric product code used for inventory and categorization. |
| product_name         | NVARCHAR(50)| Descriptive name of the product including relevant attributes such as model or size. |
| category_id          | NVARCHAR(50)| Identifier representing the product’s high-level category. |
| category             | NVARCHAR(50)| Broad classification used to group related products (e.g., Bikes, Components). |
| subcategory          | NVARCHAR(50)| More detailed classification within the main product category. |
| maintenance_required | NVARCHAR(50)| Indicates whether the product requires maintenance (Yes or No). |
| cost                 | INT         | Base cost or standard price of the product. |
| product_line         | NVARCHAR(50)| Product line or series to which the product belongs (e.g., Road, Mountain). |
| start_date           | DATE        | Date when the product became available for sale or use. |

---

## 3. gold.fact_sales

### Description
This fact table captures sales transaction data and serves as the foundation for revenue, order, and quantity-based analysis.

### Columns

| Column Name   | Data Type    | Description |
|---------------|-------------|-------------|
| order_number  | NVARCHAR(50)| Unique alphanumeric identifier assigned to each sales order. |
| product_key   | INT         | Foreign key linking the transaction to the product dimension. |
| customer_key  | INT         | Foreign key linking the transaction to the customer dimension. |
| order_date    | DATE        | Date on which the sales order was placed. |
| shipping_date | DATE        | Date when the order was shipped to the customer. |
| due_date      | DATE        | Date by which payment for the order is due. |
| sales_amount  | INT         | Total monetary value of the sales line item in whole currency units. |
| quantity      | INT         | Number of product units included in the sales order line. |
| price         | INT         | Price per unit of the product for the sales transaction. |

