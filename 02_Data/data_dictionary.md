# NYC Taxi Data Dictionary

## Dataset

**Dataset:** NYC Yellow Taxi Trip Record Data  
**Source:** NYC Taxi & Limousine Commission (TLC)  
**Project Period:** 03/08/2025 — Present

---

## Overview

This data dictionary documents the main fields expected in the NYC Yellow Taxi Trip Record dataset used for this project.

The fields describe trip timing, locations, passenger information, distance, fares, payment methods, and other trip-level characteristics.

---

## Core Variables

| Column | Description | Data Type |
|---|---|---|
| `VendorID` | Identifier for the technology provider that provided the trip record | Integer |
| `tpep_pickup_datetime` | Date and time when the meter was engaged | Datetime |
| `tpep_dropoff_datetime` | Date and time when the meter was disengaged | Datetime |
| `passenger_count` | Number of passengers reported by the driver | Numeric |
| `trip_distance` | Elapsed trip distance reported by the taximeter | Numeric |
| `RatecodeID` | Final rate code in effect for the trip | Integer |
| `store_and_fwd_flag` | Indicates whether the trip record was stored before being sent to the vendor | Categorical |
| `PULocationID` | TLC Taxi Zone where the trip started | Integer |
| `DOLocationID` | TLC Taxi Zone where the trip ended | Integer |
| `payment_type` | Method used to pay for the trip | Integer / Categorical |
| `fare_amount` | Time-and-distance fare calculated by the meter | Numeric |
| `extra` | Miscellaneous extras and surcharges | Numeric |
| `mta_tax` | MTA tax automatically triggered based on the fare | Numeric |
| `tip_amount` | Tip amount automatically populated for credit-card transactions | Numeric |
| `tolls_amount` | Total amount of tolls paid during the trip | Numeric |
| `improvement_surcharge` | Improvement surcharge assessed on the trip | Numeric |
| `total_amount` | Total amount charged to passengers, excluding cash tips | Numeric |
| `congestion_surcharge` | Congestion surcharge applied where applicable | Numeric |
| `airport_fee` | Airport-related fee where applicable | Numeric |

---

## Derived Variables

During the analysis, additional variables may be created from the original data.

| Derived Variable | Description |
|---|---|
| `trip_duration_minutes` | Trip duration calculated from pickup and drop-off timestamps |
| `pickup_hour` | Hour extracted from pickup time |
| `pickup_day` | Day of the week extracted from pickup time |
| `pickup_month` | Month extracted from pickup time |
| `fare_per_mile` | Fare amount divided by trip distance |
| `tip_percentage` | Tip amount expressed as a percentage of the fare |
| `is_peak_hour` | Indicator identifying peak operating periods |

---

## Data Quality Rules

The following checks will be considered during data cleaning:

- Pickup time must occur before drop-off time.
- Trip duration must be greater than zero.
- Trip distance should be greater than zero for completed trips.
- Fare amounts should be evaluated for negative or zero values.
- Passenger counts should be checked for unrealistic values.
- Extreme trip distances should be investigated.
- Missing critical fields should be documented and handled appropriately.
- Duplicate records should be investigated.
- Outliers should be reviewed before removal.

---

## Important Notes

Column availability can vary slightly by TLC release or taxi-data period.

The official TLC documentation should be consulted when working with a specific downloaded data file.

This dictionary is intended as a project reference and will be updated if the actual dataset contains additional or differently named fields.

---

## Source

NYC Taxi & Limousine Commission (TLC) — Trip Record Data.

This is an independent data-analysis portfolio project and is not an official publication of the City of New York or the NYC Taxi & Limousine Commission.
