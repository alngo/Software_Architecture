### What is a database?

Persistence data

#### Structured Data

Structured

#### Unstructured Data

Everything like media, img video etc...
Use for data

#### Relational database
SQL
ACID (Atomicity, Consistency, Isolation, Durability)
 - State A -> State B if all is ok
Strong consistency
Store relationship

MySQL


e.g: User information

#### NO SQL
Easy scalable
Easy setup
Handle huge amount of read/write
Eventually consitency

Redis, MongoDB
Highly available

e.g: twitter and like/repost mechanism

#### Polygot persistence

>Polyglot persistence means using several different persistence technologies to fulfil different persistence requirements in an application.


#### Different type
- Relational Database (user information, his friend, etc...)
	- MySQL
	- MariaDB
	- Amazon Aurora
	- Google Cloud SQL
- Key Value Store (caching redis, memcache)
	- Redis
	- Hazelcast
	- Riak
	- Voldemort
	- Memcache
- Wide Column database (user behavior analytics, Cassandra, Hbase)
	- Cassandra
	- HBase
	- Google BigTable
	- Scylla DB
- Graph Database (Enhance user experience)
	- Neo4j
- Document Oriented Store (ElasticSearch, enable the user to search through the data)
	- MongoDB
	- CouchDB
	- OrientDB
	- Google Cloud Datastore
	- Amazon Document DB
- Time Series Database
	- Influx DB
	- Timescale DB
	- Prometheus
- Multi-Model Database
	- Arango DB
	- Cosmos DB
	- Orient DB
	- Couchbase

#### Multi model database
