# 🏗️ Data Warehouse Project (Bronze–Silver–Gold)


This repository contains a simple data warehouse implementation based on the Medallion Architecture. The project demonstrates how raw data from multiple source systems is processed through structured layers to produce business-ready datasets.
<img width="816" height="582" alt="Data_Wearhouse_Project drawio" src="https://github.com/user-attachments/assets/9d847daf-5dce-4a41-8be1-b4e828419ffd" />


## 📖 Project Overview

The data warehouse is designed using three logical layers:

- **Bronze Layer**: Stores raw data ingested directly from source systems without transformation.
- **Silver Layer**: Contains cleaned, standardized, and validated data.
- **Gold Layer**: Provides curated, business-aligned data models for analysis and querying.

The architecture ensures clear data lineage, improved data quality, and scalability.

---

## 🗄️ Data Sources

The project uses data from the following systems:
- **CRM**: Sales transactions, customer details, and product information
- **ERP**: Product catalog, customer demographics, and location data

All source data is provided as CSV files.

---
## 🔄 Data Processing Flow

- Data is ingested into the **Bronze layer** as raw tables.
- The **Silver layer** applies cleansing, standardization, and enrichment.
- The **Gold layer** creates analytical structures such as fact and dimension tables.

This layered approach separates raw data handling from business logic and analytics.

<img width="705" height="361" alt="dataflow drawio" src="https://github.com/user-attachments/assets/4be0f20f-a9fd-4818-8918-3acaafd71df1" />


## 📐 Data Modeling

- Fact tables store transactional data (e.g., sales).
- Dimension tables store descriptive data (e.g., customers, products).
- The final model follows a star schema optimized for analytical queries.

<img width="904" height="561" alt="dataConection drawio" src="https://github.com/user-attachments/assets/a238c03e-ae1d-478a-8aa9-2e32c8b72a34" />

## 📁 Repository Structure

```
data-warehouse-project/
│
├── datasets/        # Source CSV files
├── docs/            # Architecture and data model diagrams
├── scripts/         # SQL scripts for Bronze, Silver, and Gold layers
├── README.md
└── LICENSE
```



---

## 🛡️ License

This project is licensed under the MIT License.


---

## 👨‍💻 Author

Gaurav Mali  
Aspiring Data Scientist | Python | SQL | Machine Learning

If you found this project useful, consider giving it a ⭐ on GitHub.


