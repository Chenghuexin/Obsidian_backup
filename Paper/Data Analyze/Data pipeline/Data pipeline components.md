---
work progress:
---

# 1. Origin

> [!NOTE]
> ## Definition : The start of data in the pipeline
> - different type of data source
> - storage systems

# 2. Destination

> [!NOTE] ## Definition : The data after transfering
> - depends mainly on the practical application of the data

# 3. Dataflow

> [!NOTE] ## Definition : The process of data "flowing" between the starting point and the ending point
> ### ETL
> - Extract : Get data from disparate source systems
> - Transform : Move data into **staging area** and convert data format into a future usable format 
> - Load : load reformatted data to final destination

# 4. Storage

> [!NOTE] ## Definition : The place where data is stored at different stages in the pipeline
> ### depends on many factors(example) : 
> - volume
> - fequency
> - volume of queries to a storage system

# 5. Processing

> [!NOTE] ## Definietion : How to **implement** the process of data changes
> ### Example : 
> - database replication
> - streaming data

# 6. Workflow
>[!NOTE] ## Definition : In the pipeline, workflow defines a series of tasks and dependence between data
>## Concept : 
>- job
>- upstream
>- downstream

# 7. Monitoring
>[!NOTE] ## Definition : Check whether the data in the pipeline is functioning normally
>## Example : 
>- efficiency
>- data load

# 8. Technology
>[!NOTE] 
>## 1. ETL  tools : data preparation, integration tools
>	Informatica Power Center, 
>	Apache Spark, 
>	Talend Open Studio
>## 2. Data warehouses : RDBMS
>	Amazon Redshift, 
>	Snowflake, 
>	Oracle
>## 3. Data lakes : Raw data storage, which may be relational or non-relational data
>	Microsoft Azure, 
>	IB
>## 4. Batch workflow schedulers: Automate and monitor workflows
>	Airflow, Luigi, 
>	Oozie, 
>	Azkaban
>## 5. Handle streaming/continuously generated data
>	Apache Spark, 
>	Flink, 
>	Storm, 
>	Kafka
>## 6. Programming Language
>	java
>	python
>	Ruby
>	Scala
>	 		
