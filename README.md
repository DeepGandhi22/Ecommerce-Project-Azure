# Ecommerce Data Engineering Project
## Goal
The main goal of this project is to develop an end to end Data Engineering Pipeline to fetch the data from various sources, transform, enrich and store the important data utilizing various Microsoft Azure tools and services.

## Project Architecture
![DataArchitecture](https://github.com/user-attachments/assets/fd679227-e6fa-4159-b949-375c02dff88d)


The above diagram illustrates the pipeline I created to complete this project.  
This pipeline follows the **Bronze-Silver-Gold** layered architecture to manage raw, refined, and curated data efficiently.

---

## Pipeline Overview

### 1. Data Ingestion - Azure Data Factory
Azure Data Factory was used to ingest data from **GitHub**, **Azure SQL Database**, and store raw files in the **Bronze** container.

![DataFactory_Ingesion](https://github.com/user-attachments/assets/5682c910-3b58-412d-8f05-434666061e0d)


---

### 2. Data Enrichment & Transformation - Azure Databricks
The raw data was enriched by pulling in additional data from **MongoDB**, and then transformed using **Azure Databricks (PySpark)**. The processed data was stored in the **Silver** container.

---

### 3. Data Modeling - Azure Synapse Analytics
Using **Azure Synapse Analytics**, various SQL views and aggregations were created from the silver layer and stored in the **Gold** container for reporting purposes.

  ![Synapse_Transfer](https://github.com/user-attachments/assets/0bae2e4b-959e-4215-b7c5-f72feaaba3db)



---

### 4. Data Visualization
The final curated data in the **Gold** container can be visualized using tools like **Power BI**, allowing for interactive dashboards and reporting.

---

## Technologies Used
- **Microsoft Azure**
  - Azure Data Factory
  - Azure Blob Storage (Bronze, Silver, Gold)
  - Azure Databricks (PySpark)
  - Azure Synapse Analytics
- **GitHub** – Source for CSV data
- **Azure SQL Database** – Additional data source
- **MongoDB** – For enrichment
- **Power BI** (optional) – For data visualization

---

## Learnings
Through this project, I gained hands-on experience with various Azure services, built a production-style data pipeline, and learned how to structure data workflows using the Bronze-Silver-Gold architecture commonly adopted in modern data engineering.

---
