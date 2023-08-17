Hands on Project for Data Engineers using all the services available in Azure Synapse Analytics


Currently the course teaches the following

- Azure Synapse Analytics Architecture
- Serverless SQL Pool
- Spark Pool
- Dedicated SQL Pool
- Synapse Pipelines
- Synapse Link for Cosmos DB / Hybrid Transactional and Analytical Processing (HTAP) capability
- Power BI Integration with Azure Synapse Analytics
- Azure Data Lake Storage Gen2 integration with Azure Synapse Analytics
- Project using NYC Taxi Trips data using the above technologies

So we need to provide the ability to perform exploration of the raw data. We want to make it easier for the Data Analyst to explore this data. So instead of providing the raw files as
they are, we should apply the schema to the data so that it's easier to understand the data and gain business value from it. To support the Business Analysts who are already familiar 
with the Microsoft T-SQL language, we should offer the capability to perform Data Discovery using T-SQL. And finally, the business doesn't want to pay for any dedicated resources at 
this stage of the project. They want us to offer the ability to query this data using pay-per-query model via the serverless infrastructure, and then they may decide to use dedicated
resources based on the business value.

We want to ingest all of the seven files that we talked about spanning the various data formats. The data ingested into our Data Lake should confirm to the following requirements.
We should ingest the data into the Data Lake and store that in a columnar format such as Parquet, so that it performs better with analytical queries. We should apply the right schema to 
the data including column names and data types. Also, we should create tables or views of the data so that it is easier to analyse and report from.

We should provide the ability to query the data using T-SQL alongside other query engines such as Spark and Data flows. The Ingestion should again be done using the pay-per-query model 
rather than using dedicated resources.

Transformation requirements:

We need tables that provide the data joined from the key data items that are required for reporting. For example, data from trips and taxi zones combined, so that we can produce BI 
reports from this table. Similarly, we need tables and data sets with the data joined that to satisfy the analytical requirements, also transform data must be available for consumption
via T-SQL for ease of use for both analysis as well as BI tools. And finally, the transformed data should be stored in columnar format such as Parquet.


BI reporting requirements:

We want to produce a report to identify the demand for taxis during days of weeks as well as in different locations in the city, etc..
We also want to produce a report to help with a campaign to encourage credit card payments as supposed to cash.
We also want to build the capability to enable operational reporting on the data from the IoT devices on the taxis.


Nonfunctional requirements:

We want to schedule the pipeline to run at regular intervals.
We want to have the ability to monitor the status of the pipeline executions, rerun failed pipelines, as well as the ability to set up alerts on failures.
