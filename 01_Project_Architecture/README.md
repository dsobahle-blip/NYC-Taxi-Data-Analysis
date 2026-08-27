# 01 — Project Architecture

## Overview

This folder documents the architecture of the NYC Taxi Data Engineering
project built using Microsoft Fabric.

## Architecture

The project follows the Medallion Architecture:

```text
NYC Taxi Dataset
       │
       ▼
Microsoft Fabric
       │
       ▼
Bronze Layer
Raw / Ingested Data
       │
       ▼
Silver Layer
Cleaned / Transformed Data
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
       │
       ▼
Business Dashboard
