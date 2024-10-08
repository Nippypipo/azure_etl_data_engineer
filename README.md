Hello, today I'm going show my ETL pipeline project that I learned during my summer internship 2024 as a Data Engineer intern at BBIK.

You can read a detailed explanation of this project in this medium article: [สร้าง ETL Pipeline ด้วย Microsoft Azure | End-to-end Data Engineer Project](https://medium.com/@nipunaungkawichai_54820/%E0%B8%AA%E0%B8%A3%E0%B9%89%E0%B8%B2%E0%B8%87-etl-pipeline-%E0%B8%94%E0%B9%89%E0%B8%A7%E0%B8%A2-microsoft-azure-end-to-end-data-engineer-project-554c3c90914c)

# Overview
This project overview involves creating an ETL pipeline from extracting data from the data source to delivering quality data for presentation in a PowerBI dashboard, primarily using Microsoft Azure: Cloud Computing Services.
![Alt text](pictures/overview_de_project.png)

For the ETL process in this project, it includes extracting data from the data source (SQL Server), followed by data transformation at the staging area (Data Lake), before loading it into the Lakehouse (Delta Lake)


# Process
The process overview can be summarized as follows:

- **Ingestion:** Extract data from various data sources, such as SQL Server, to store in the staging area and merge the data into the Lakehouse.
- **Transformation:** Transform the data in the Lakehouse into a format that is ready for analysis.
- **Serving:** Connect the data from the Lakehouse to a BI tool like PowerBI to create dashboards according to business requirements.

# Techstack

![Alt text](pictures/techstack_de_project.jpg)
# Code
You can find the code at the link below.

T-SQL Stored Procedure
- [MergeMetadata.sql](https://github.com/Nippypipo/Azure_ETL_Data_engineer_Project/blob/main/sql_stored_procedures/MergeMetadata.sql)
- [PayloadGenerator.sql](https://github.com/Nippypipo/Azure_ETL_Data_engineer_Project/blob/main/sql_stored_procedures/PayloadGenerator.sql)
- [UpdateCleansedData.sql](https://github.com/Nippypipo/Azure_ETL_Data_engineer_Project/blob/main/sql_stored_procedures/UpdateCleansedData.sql)
- [UpdateMetadata.sql](https://github.com/Nippypipo/Azure_ETL_Data_engineer_Project/blob/main/sql_stored_procedures/UpdateMetadata.sql)

Spark Notebook
- [main_merge_pipeline.ipynb](https://github.com/Nippypipo/Azure_ETL_Data_engineer_Project/blob/main/spark_notebook/main_merge_pipeline.ipynb).
- [merge_functions.ipynb
](https://github.com/Nippypipo/Azure_ETL_Data_engineer_Project/blob/main/spark_notebook/merge_functions.ipynb)
- [test_merge_functions.ipynb](https://github.com/Nippypipo/Azure_ETL_Data_engineer_Project/blob/main/spark_notebook/test_merge_functions.ipynb)

