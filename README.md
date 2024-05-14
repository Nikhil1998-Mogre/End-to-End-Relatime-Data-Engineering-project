The tools we will be using in this project are:

1) Azure Data Factory
2) Azure Synapse Analytics
3) Azure Databricks
4) Azure Data Lake
5) Azure Active Directory
6) Azure Key Vault
7) Power BI

Step by Step approach for the project

1. In the data engineering project described, an on-premise MYSQL database is connected to Azure Data Factory using a self-hosted integration runtime(SHIR). This integration runtime is installed on the same machine where the MYSQL database is hosted, allowing Azure Data Factory to securely connect to the on-premise database.


<img width="893" alt="Screenshot 2024-05-06 172812" src="https://github.com/Nikhil1998-Mogre/End-to-End-Relatime-Data-Engineering-project/assets/109106842/12886f64-8a2a-46cd-80a0-0518c70b7ee4">

2. We will be using Azure Data Lake Gen 2 as the storage solution in Azure, and the data that is stored in Azure Data Lake.

3. Once the data has been added to Azure Data Lake, we will be using Azure Databricks to transform the raw data into curated data. Azure Databricks is a big data analytics tool that is useful for high-end data analytics workloads. We can write code in SQL, PySpark, or Python in Azure Databricks to transform the data.

4. In Azure Databricks, we will also be implementing a concept called lakehouse architecture. In this architecture, Azure Data Lake will be divided into multiple layers. The first layer is the bronze layer, which has an exact copy of what the data looks like in the data source. We will not touch any data in the bronze layer, and we will not change the format or anything inside the bronze layer. This layer serves as the source of truth, and if something goes wrong in the subsequent data transformations, we can come back to this bronze layer and get all the data to try out, which will be the same as the data source.

   <img width="959" alt="copytodatabricks_snapshot" src="https://github.com/Nikhil1998-Mogre/End-to-End-Relatime-Data-Engineering-project/assets/109106842/eca52929-b0e2-4f27-9f34-852015bfcb7b">

5. Once the data has been loaded to the gold layer, we will then use Azure Synapse Analytics to create a similar data model as the on-premise SQL database. This will allow us to query the data in Azure Synapse Analytics just like we would in the on-premise SQL database.

Finally, we will be using Power BI to create reports and visualizations on the data that has been stored in Azure Synapse Analytics. Power BI is a powerful tool that can be used to create different kinds of reports, charts, and visualizations on the data.

