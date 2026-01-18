# Data Warehouse Project (Bronze–Silver–Gold)

This repository showcases a simple data warehouse implementation following the Medallion Architecture. The project demonstrates how raw data from multiple source systems is processed through structured layers to produce analytics-ready data.

---

## High-Level Architecture

The overall architecture consists of three logical layers inside the data warehouse.

![High Level Architecture](Data_Wearhouse_Project.drawio.png)

- **Bronze Layer**: Raw data ingestion from source systems.
- **Silver Layer**: Cleaned and standardized data.
- **Gold Layer**: Business-ready data for analysis.

---

## Data Flow

The data flows sequentially from source systems into the Bronze layer, then into Silver, and finally into Gold for consumption.

![Data Flow](dataflow.drawio.png)

---

## Data Integration

Data from CRM and ERP systems is integrated using common business keys to form a unified analytical model.

![Data Integration](dataConection.drawio.png)

---

## Repository Structure

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

## License

This project is licensed under the MIT License.
