# Databases

## Relational Database Service \(RDS\)

#### Types:

* SQL Server
* Oracle
* MySQL Server
* PostgreSQL

**Aurora** \(Amazon's own database\):

* Creates 6 copies of itself
* 5 times better performance than MySQL, 1/10 price point
* Choose Aurora if you have an RDS
* MariaDB

Two key features:

1. Multi availability zones for disaster recovery: Exact copy of your database in case the primary goes down \(Disaster recovery\)
2. Read replicas for performance improvement: Spread read access across five databases, only one is for writing \(Scaling out / performance\)

## Non-relational Databases \(NoSQL\)

* Collection \(table\)
* Documents \(row\)
* Key-value pairs \(fields\)
* Allows you to add in extra fields all the time

**Amazon DynamoDB** is Amazon's nonrelational/NoSQL database

* Fast \(low latency\), flexible
* Scales with your application

**DocumentDB**

* A fully managed document database service that supports MongoDB workloads.

## Data Warehousing \(Redshift\)

* Used for business intelligence
* Used to pull in large and complex datasets
* Used by management to do queries \(current performance targets, etc\)
* Amazon's data warehouse in the cloud for business intelligence
  * Start with a few hundred GB of data, scale to petabyte or more

