# Naming Standards

This document defines the naming rules used for schemas, tables, views, columns, and other objects in the data warehouse.

## General Guidelines
- Use snake_case with lowercase letters and underscores (_) to separate words.
- Use English for all object names.
- Avoid using SQL reserved keywords as object names.

## Table Naming Standards

### Bronze Layer
- Table names must start with the source system name.
- Source table names must remain unchanged.
- Format: <source_system>_<entity_name>
- Example: crm_customer_info

### Silver Layer
- Table names must start with the source system name.
- Source table names must remain unchanged.
- Format: <source_system>_<entity_name>
- Example: crm_customer_info

### Gold Layer
- Table names must use meaningful, business-oriented names.
- Names must start with a category prefix.
- Format: <category>_<entity_name>
- Examples:
  - dim_customers
  - fact_sales

## Category Prefix Reference
| Prefix  | Description       | Example(s)                  |
|---------|-------------------|-----------------------------|
| dim_    | Dimension table   | dim_customer, dim_product   |
| fact_   | Fact table        | fact_sales                  |
| report_ | Reporting table   | report_sales_monthly        |

## Column Naming Standards

### Surrogate Keys
- All surrogate primary keys must end with _key.
- Format: <entity_name>_key
- Example: customer_key

### Technical Columns
- All technical or system-generated columns must start with dwh_.
- Format: dwh_<column_description>
- Example: dwh_load_date

## Stored Procedure Naming
- Stored procedures used for data loading must follow the pattern load_<layer>.
- Example:
  - load_bronze
  - load_silver
