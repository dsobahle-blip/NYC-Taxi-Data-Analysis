# 03 — Data Cleaning

## NYC Taxi Data Preparation

**Project Period:** 03/08/2025 — Present  
**Project Stage:** Data Cleaning & Preparation

---

## 📌 Purpose

The purpose of this stage is to transform the raw NYC taxi trip data into a reliable and analysis-ready dataset.

Real-world datasets can contain missing values, duplicate records, invalid measurements, inconsistent timestamps, and extreme observations.

Before performing exploratory analysis, the data must therefore be inspected, validated, and cleaned.

---

## 🎯 Cleaning Objectives

The cleaning process will focus on:

- Understanding the structure of the raw dataset
- Identifying missing values
- Detecting duplicate records
- Validating date and time fields
- Checking trip distances
- Checking trip durations
- Validating passenger counts
- Reviewing fare amounts
- Identifying extreme values and outliers
- Creating useful analytical variables

---

## 🔎 Data Quality Checks

### 1. Missing Values

Missing values will be identified across all important columns.

Particular attention will be given to:

- Pickup time
- Drop-off time
- Pickup location
- Drop-off location
- Trip distance
- Fare amount
- Payment type

Missing values will be assessed based on their importance to the analysis before deciding whether to remove, replace, or retain them.

---

### 2. Duplicate Records

Duplicate records will be investigated to determine whether they represent:

- Exact duplicate rows
- Legitimate repeated trips
- Data-processing issues

Confirmed duplicates may be removed where appropriate.

---

### 3. Date & Time Validation

Pickup and drop-off timestamps will be converted into appropriate datetime formats.

The following checks will be performed:

- Pickup time must occur before drop-off time.
- Trip duration must be greater than zero.
- Extremely long durations will be investigated.
- Invalid timestamps will be removed or flagged.

---

### 4. Trip Distance Validation

The `trip_distance` field will be reviewed for:

- Zero-distance trips
- Negative values
- Extremely large distances
- Potential data-entry errors

Unusual observations will be investigated before removal.

---

### 5. Passenger Count Validation

Passenger counts will be examined for:

- Missing values
- Zero passengers
- Negative values
- Unrealistic passenger counts

Records that appear inconsistent with normal taxi operations will be reviewed as potential anomalies.

---

### 6. Fare Validation

Fare-related fields will be checked for:

- Negative fares
- Zero fares
- Extremely high fares
- Unusual surcharge values
- Inconsistent total amounts

These checks will help prevent distorted pricing analysis.

---

## 🧮 Derived Variables

Additional variables will be created to support analysis.

Examples include:

| Variable | Purpose |
|---|---|
| `trip_duration_minutes` | Measures trip duration |
| `pickup_hour` | Identifies hourly demand patterns |
| `pickup_day` | Identifies day-of-week patterns |
| `pickup_month` | Identifies monthly trends |
| `fare_per_mile` | Measures pricing relative to distance |
| `tip_percentage` | Measures tipping behavior |
| `is_peak_hour` | Identifies peak operating periods |

---

## 📊 Before & After Comparison

The cleaning process will document:

| Metric | Before Cleaning | After Cleaning |
|---|---:|---:|
| Total Records | TBD | TBD |
| Missing Values | TBD | TBD |
| Duplicate Records | TBD | TBD |
| Invalid Trips | TBD | TBD |
| Outliers Reviewed | TBD | TBD |

Actual values will be added after the dataset has been processed.

---

## 🛠️ Tools

The cleaning process will use:

- Python
- Pandas
- NumPy
- Jupyter Notebook
