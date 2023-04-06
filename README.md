# OList_Business_Data_Analysis


**Data Model**: Relational DB (SQL Server) 


**Target Platform**: Azure Cosmos DB (API) 

**Implementation**:

o	We conducted data profiling, data cleaning, and ETL tasks using Talend to transform unstructured data from CSV files into Microsoft SQL Server. Then, we employed a Python script to convert SQL reports into JSON format, utilizing Cosmos DB for SQL API, and scheduled this script in Apache Airflow orchestration tool by configuring the DAG.

o	After the JSON files were generated, they were loaded into Azure Blob storage containers by the script. The creation of a new blob triggered the Azure Data Factory Copy Job, which loaded the JSON data into the corresponding Azure Cosmos DB container using the MERGE operation.

o	Finally, we used the Gremlin Python API to transfer the SQL reports into the Azure Cosmos Gremlin Graph Database and established the edge relationships between the nodes.


**Objective/Scope**:

• Analyzing top selling product categories

• Study of product sales by geographical locations

• Comparing seller’s sales data by locality and time

• Analyzing customer review ratings for authorized Olist sellers

• Analyzing company sales revenue

• Identifying the customer payment methods

• Average delivery time by geographical location


**Visualization Tool**: Power BI
