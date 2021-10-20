---
title: 'Databases'
metaTitle: 'Databases. Their features, use cases and pricing models.'
metaDescription: 'Databases. Their features, use cases and pricing models.'
---

## Relational Database Service (RDS)

Makes it easy to launch and manage relational databases.

- Supports popular **database engines**.
  - Aurora
  - Postgres
  - MySQL
  - MariaDB
  - Oracle
  - SQL Server
- AWS manages the database with automatic patching, automated backups, operating system maintenance, and more.
- Allows you to launch **read replicas** across regions to provide enhances performance and durability.
  - A **Read Replica** is a **read-only** copy of your database for fast querying.

## Amazon Aurora

**Aurora **is a relational database compatible with **MySQL** and **PostgreSQL** that was created by **AWS**.

- Suports **MySQL** and **PostgreSQL** database engines.
- **5 times** faster than normal MySQL and **3x** faster than normal PotsgreSQL.
- **Scales Automatically** while providing durability and high availability.
- It's managed by **RDS** so you get all the out of the box services RDS provides.

## Amazon DynamoDB

**DynamoDB** is a fully managed **NoSQL** key-value and document database.

- A **NoSQL** database simply means it is a self describing database and it doesn't enforce relations between tables like a relational database.
- Fully managed and **serverless**.
- **Scales automatically** to massive workloads with **fast** performance.

## Amazon DocumentDB

**DocumentDB** is a fully managed document database that supports **MongoDB**.

- It's a **document database**
- Fully managed and **serverless**.
- Non-relational.

## Amazon ElastiCache

**ElastiCache** is a fully managed in-memory datastore compatible with **Redis** or **Memcached**.

Can be used to reduce load on a regularily read intensive database.

- In memory datastore.
- Data can be lost (cause it's in memory).
- High performance and low latency.

## Amazon Neptune

**Neptune** is a fully managed **graph database** that supports highly connected datasets.

- Fit for data that relates in a network.
- Fully managed and serverless.
- **Fast and reliable**.
