### Stream

Massive amount of data, need to be treated real quick

Several method

#### Data ingestion

>Data Ingestion is a collective term for the process of collecting data streaming-in from several different sources and making it ready to be processed by the system

Several layer
- Data collection layer
- Data query layer
- Data processing layer
- Data visualization layer
- Data storage layer
- Data security layer

##### Data Standardization (collection layer)

uniform all incoming data to have a consistent standard format

##### Data Processing

Classify and route into different flow

##### Data Analysis

Run analytic, model, statistical

##### Data visualization

Kibana!

##### Data Storage & Security

Secure data's movement through the different layer

#### Way to ingest data

Realtime less accurate (take set of data) but faster
Batch more accurate (take all data) but slower

[Linkedin gobblin](https://engineering.linkedin.com/data-ingestion/gobblin-big-data-ease)
Hadoop

#### Data pipeline
>Data pipelines are the core component of a data processing infrastructure. They facilitate the efficient flow of data from one point to another & also enable the developers to apply filters on the data streaming-in in real-time.

Extract Transform Load (ETL)

- Extract means fetching data from single or multiple data sources.
- Transform means transforming the extracted heterogeneous data into a standardized format based on the rules set by the business.
- Load means moving the transformed data to a data warehouse or another data storage location for further processing of data.

[Netflix](https://www.infoq.com/articles/netflix-migrating-stream-processing/)

#### Distributed Data Processing

>Distributed data processing means diverging large amounts of data to several different nodes, running in a cluster, for parallel processing.

Tech: (Cluster computing)
- MapReduce (Hadoop)
- Apache Spark
- Apache Storm
- Apache Kafka
