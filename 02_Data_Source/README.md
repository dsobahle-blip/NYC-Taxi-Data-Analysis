# 02 — NYC Taxi Data Source

## Overview

This project uses NYC Taxi trip data to demonstrate an end-to-end data
engineering and analytics solution using Microsoft Fabric.

The dataset contains taxi trip records that can be used to analyse
transportation patterns, trip activity, fares, distances, payment methods
and time-based travel behaviour.

---

## Data Engineering Objective

The objective is to ingest, transform, validate and analyse NYC Taxi data
using Microsoft Fabric.

The data follows a Medallion Architecture:

```text
NYC Taxi Dataset
       │
       ▼
Bronze Layer
Raw Data
       │
       ▼
Silver Layer
Cleaned Data
       │
       ▼
Gold Layer
Business-Ready Data
       │
       ▼
SQL Warehouse
       │
       ▼
Semantic Model
       │
       ▼
Power BI
