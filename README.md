# Mircosoft Farbric End to End Pipeline 

##  Project Overview
This project demonstrates a complete **end-to-end Power BI analytics solution** built using the **Medallion Architecture** approach (Bronze, Silver, and Gold layers).Data is ingested into **Lakehouses** using **Power BI Dataflows**, progressively refined across layers, exposed through a **Semantic Model**, and finally visualized in a **Power BI report**.  The architecture follows industry best practices for **scalability, data quality, governance, and performance**.

##  Architecture Overview


## 🥉 Bronze Layer – Raw Data

### Purpose
- Capture raw data from source systems
- Preserve original structure and history
- Enable reprocessing and auditing

### Characteristics
- Minimal or no transformations
- Append-only ingestion
- Schema-on-read

### Implementation
- Power BI Dataflows ingest source data
- Data stored in the Bronze Lakehouse

-

## Silver Layer – Cleaned & Transformed Data

### Purpose
- Improve data quality
- Apply business logic
- Standardize data formats

### Transformations
- Data type validation
- Null handling
- Deduplication
- Column renaming and standardization

### Implementation
- Power BI Dataflows read from Bronze Lakehouse
- Cleaned data written to Silver Lakehouse

-

## Gold Layer – Business-Ready Data

### Purpose
- Prepare data for analytics and reporting
- Optimize performance
- Enable reusable datasets

### Characteristics
- Aggregated fact tables
- Conformed dimension tables
- Star-schema–friendly design

### Implementation
- Power BI Dataflows read from Silver Lakehouse
- Curated datasets stored in Gold Lakehouse

-

##  Semantic Model

### Purpose
- Serve as a single source of truth
- Enable consistent reporting and self-service analytics
- Improve query performance

### Features
- Defined relationships between fact and dimension tables
- DAX measures and KPIs
- Calculated columns and hierarchies
- Optional Row-Level Security (RLS)

### Implementation
- Semantic Model built on top of Gold Lakehouse tables

-

##  Power BI Report

### Purpose
- Deliver business insights
- Enable interactive data exploration

### Technologies Used
- Power BI Dataflows
- Lakehouse Architecture
- Medallion Architecture
- DAX
- Power BI Semantic Model
- Power BI Reports






