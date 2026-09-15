# 🛒 E-Commerce ETL Pipeline - Medallion Architecture

> Production-style ETL pipeline built with Python & Pandas following Bronze → Silver → Gold pattern

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Pandas](https://img.shields.io/badge/Pandas-ETL-green)
![Architecture](https://img.shields.io/badge/Architecture-Medallion-orange)

### 🎯 Problem Statement
Real-world e-commerce data is dirty. This project simulates real issues:
- Duplicate orders (100 duplicate rows)
- Missing prices (NaN values)
- Dirty dates & inconsistent formats
- Need for business-ready KPIs

### 🏗️ Architecture - Medallion

**Bronze (Raw):** `data/bronze/orders_raw.csv` - 5100 rows ingested as-is from source
**Silver (Clean):** `data/silver/orders_clean.parquet` - Deduplicated, NaN handled, Parquet optimized
**Gold (Business):** `data/gold/` - Aggregated KPIs for BI dashboards
