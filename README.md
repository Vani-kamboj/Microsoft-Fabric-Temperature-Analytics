![Microsoft Fabric](https://img.shields.io/badge/Microsoft_Fabric-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)

# Microsoft Fabric - Temperature Sensor Analytics

## Overview
An end-to-end data solution built on Microsoft Fabric that ingests 
real-time temperature sensor data from an API, processes it through 
multiple layers, and delivers live dashboards with automated alerting.

## Tools & Technologies
- Microsoft Fabric (Lakehouse, Data Warehouse, Semantic Model, Data Activator)
- Python Notebooks
- Power BI

## Architecture
![Pipeline Architecture](architecture.png)

## How it works

### Data Ingestion
Temperature sensor data is fetched from an external API using 
Python Notebooks and loaded into the Lakehouse Bronze layer.

### Data Processing
- **Bronze** — Raw data as ingested from the API
- **Silver** — Cleaned and validated data
- **Gold** — Aggregated and business-ready data

### Data Warehouse
Gold layer data is moved into the Data Warehouse using pipelines, 
where SQL tables and views are created for reporting.
The pipeline is scheduled to run automatically every 1 hour, 
ensuring the data is always up to date.

### Semantic Model
A semantic model is auto-generated from the Data Warehouse, 
which is directly used in Power BI for live reporting.

### Alerting
Data Activator monitors temperature readings and automatically 
sends email alerts to the team when temperature crosses the threshold.

## Files
- `fabric_workflow.png` — End-to-end pipeline architecture diagram
