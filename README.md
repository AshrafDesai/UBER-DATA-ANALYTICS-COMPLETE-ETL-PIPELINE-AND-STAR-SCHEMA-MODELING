# UBER-DATA-ANALYTICS-COMPLETE-ETL-PIPELINE-AND-STAR-SCHEMA-MODELING

<img width="975" height="642" alt="image" src="https://github.com/user-attachments/assets/235d7feb-7161-43f3-a75b-1c8a33c29739" />

## Project Overview

The objective of this project is to design and implement a complete end-to-end Data Engineering pipeline using modern big data technologies. The solution demonstrates:

* Raw data ingestion using Databricks Volumes

* Implementation of Medallion Architecture (Bronze, Silver, Gold)

* Data transformation and cleansing using Apache Spark

* Dimensional modeling using Star Schema

* Fact and Dimension table design

* Delta Lake optimization and partitioning

* Interactive Power BI dashboards for analytics

This project simulates a real-world enterprise data platform used for scalable data processing and business intelligence reporting.

## Technology Stack

| Component          | Technology                    |
|--------------------|-------------------------------|
| Platform           | Databricks                   |
| Processing Engine  | Apache Spark                 |
| Storage Format     | Delta Lake                   |
| Architecture       | Medallion (Bronze/Silver/Gold) |
| Data Modeling      | Star Schema                  |
| Visualization      | Power BI                     |
| Analytics          | DAX                          |

## Dataset Description

The dataset contains Uber trip-level transactional data. Each row represents a completed trip and includes:

* Pickup & dropoff timestamps

* Passenger count

* Trip distance

* Fare amount

* Tip amount

* Location coordinates

* Payment type

This dataset enables:

* Revenue analysis

* Peak hour identification

* Passenger behavior analysis

* Operational performance insights

## Bronze Layer – Raw Data Ingestion

### Objective:

Store raw data exactly as received.

Steps:

* Created Unity Catalog Volume

* Uploaded CSV dataset

* Loaded data using Spark

* Stored as Delta table

### Purpose:

* Preserve raw source data

* Enable reprocessing

* Maintain audit trail

## Silver Layer – Data Cleaning & Transformation

### Objective:

Clean, validate, and standardize data.

### Transformations Performed:

* Converted timestamp columns

* Removed null values

* Filtered invalid distances

* Created derived columns:

  * trip_date

  * trip_hour

  * year

  * month

  * day

### Purpose:

* Improve data quality

* Prepare for analytical modeling

* Standardize formats

## Gold Layer – Star Schema Modeling

The Gold layer contains business-ready data optimized for reporting.

## Star Schema Design

### Fact Table – fact_trips

Contains measurable metrics:

* fare_amount

* trip_distance

* tip_amount

* passenger_count

* date

* hour
* 
## Dimension Tables

### dim_date

* date

* year

* month

* month_name

* day

### dim_hour

* hour

* hour_category (Peak / Off-Peak)

### dim_passenger

* passenger_count

* passenger_type (Single / Group)

Why Star Schema?

* Faster BI queries

* Simplified relationships

* Optimized aggregations

* Industry-standard dimensional modeling

## Power BI Dashboard

Connected Power BI to Databricks Gold Layer.

### Dashboard Pages:

#### Executive Overview

* Total Revenue

* Total Trips

* Average Fare

* Revenue per KM

* Monthly Revenue Trend

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/819ed154-be2e-41a8-9212-ed49449d340f" />

#### Time & Peak Analysis

* Trips by Hour

* Revenue by Hour

* Month vs Hour Matrix

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/7681b0aa-eb35-491b-a993-18bac123294d" />

#### Operational Insights

* Distance vs Fare Scatter Plot

* Passenger Distribution

* Detailed Trip Table

  <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/b24af0af-30e6-44a1-a7c3-9845b75570f8" />

## Conclusion

This project successfully implements a complete end-to-end Data Engineering solution using modern tools and best practices. It demonstrates strong understanding of:

* Data ingestion

* ETL transformation

* Medallion Architecture

* Star Schema modeling

* Delta Lake optimization

* Power BI reporting

## Author

# Asharafraza Desai
# Data Engineering Enthusiast
