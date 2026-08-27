# 🚕 NYC Taxi Data Engineering Project

## Microsoft Fabric | Medallion Architecture | SQL | PySpark | Power BI

![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-Data%20Engineering-purple)
![PySpark](https://img.shields.io/badge/PySpark-Data%20Processing-orange)
![SQL](https://img.shields.io/badge/SQL-Analytics-blue)
![Power BI](https://img.shields.io/badge/Power%20BI-Visualization-yellow)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black)

---

## 📌 Project Overview

This project demonstrates an end-to-end data engineering and analytics
solution for NYC Taxi trip data using Microsoft Fabric.

The project follows the Medallion Architecture to transform raw taxi
data into clean, validated, business-ready data for analytics and
decision-making.

### Data Flow

Source Dataset
→ Bronze Layer
→ Silver Layer
→ Gold Layer
→ Data Warehouse
→ Semantic Model
→ Power BI
→ Business Insights

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Ingest NYC Taxi data into Microsoft Fabric.
- Build a scalable data engineering pipeline.
- Implement Medallion Architecture.
- Store raw data in the Bronze layer.
- Clean and transform data in the Silver layer.
- Create business-ready datasets in the Gold layer.
- Load analytical data into a Fabric Warehouse.
- Build a semantic model for reporting.
- Create interactive Power BI dashboards.
- Generate meaningful business insights.

---

## 💼 Business Questions

The project is designed to answer questions such as:

1. How many taxi trips were completed?
2. What is the total taxi revenue?
3. What is the average fare per trip?
4. What is the average trip distance?
5. What are the busiest pickup locations?
6. What are the busiest hours?
7. Which days generate the highest taxi demand?
8. Which payment methods are most commonly used?
9. Which locations generate the highest revenue?
10. How does taxi demand change over time?

---

# 🏗️ Solution Architecture

The project uses Microsoft Fabric and follows the Medallion Architecture.

```text
                    NYC TAXI DATASET
                           │
                           ▼
                ┌─────────────────────┐
                │  MICROSOFT FABRIC   │
                │      WORKSPACE      │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │    🥉 BRONZE        │
                │    RAW DATA         │
                │                     │
                │ Pipeline            │
                │ Copy Activity       │
                │ Dataflow Gen2       │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │    🥈 SILVER        │
                │  CLEANED DATA       │
                │                     │
                │ PySpark             │
                │ SQL                 │
                │ Dataflow Gen2       │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │     🥇 GOLD         │
                │ BUSINESS-READY DATA │
                │                     │
                │ Fact Tables         │
                │ Dimension Tables    │
                │ Aggregations        │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   DATA WAREHOUSE    │
                │       SQL           │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   SEMANTIC MODEL    │
                │                     │
                │ Relationships       │
                │ Measures            │
                │ KPIs                │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │      POWER BI       │
                │     DASHBOARD       │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ BUSINESS INSIGHTS   │
                │ & RECOMMENDATIONS   │
                └─────────────────────┘


BRONZE LAYER

NYC Taxi Dataset
       ↓
Pipeline
       ↓
Copy Activity
       ↓
Bronze Lakehouse
       ↓
Raw Taxi Data

SILVER LAYER

Bronze Data
     ↓
Data Cleaning
     ↓
Data Validation
     ↓
Data Transformation
     ↓
Silver Data

GOLD

                    DimDate
                       │
                       │
                       ▼
DimLocation ───► FactTaxiTrips ◄─── DimPaymentType
                       ▲
                       │
                       │
                    DimTime


REPOSITORY STRUCTURE

NYC-Taxi-Data-Engineering-Fabric/
│
├── README.md
│
├── 01_Project_Planning/
│
├── 02_Source_Data/
│
├── 03_Bronze_Layer/
│
├── 04_Silver_Layer/
│
├── 05_Gold_Layer/
│
├── 06_Warehouse/
│
├── 07_Semantic_Model/
│
├── 08_Power_BI/
│
├── 09_SQL/
│
├── 10_Documentation/
│
├── 11_Presentation/
│
└── images/


END TO END DATA FLOW

                SOURCE
                   │
                   ▼
              NYC TAXI DATA
                   │
                   ▼
             FABRIC PIPELINE
                   │
                   ▼
             🥉 BRONZE
                   │
                   ▼
             🥈 SILVER
                   │
                   ▼
              🥇 GOLD
                   │
                   ▼
             WAREHOUSE
                   │
                   ▼
           SEMANTIC MODEL
                   │
                   ▼
               POWER BI
                   │
                   ▼
          BUSINESS INSIGHTS
