---
layout: default
title: Database Setup
---
This guide will help you setup databases and data-related services for
your project. Every build is executed in its very own virtual machine that
comes pre-installed with the following:

* [SQLite](#sqlite)
* [MySQL](#mysql)
* [PostgreSQL](#postgres)
* [MongoDB](#mongodb)
* [Memcache](#memcache)
* [Redis](#redis)
* [Neo4j](#neo4j)
* [Elastic Search](#elasticsearch)
* [CouchDB](#couchdb)

## <a name="sqlite"></a> SQLite

SQLite3 comes pre-installed.

## <a name="mysql"></a> MySQL

MySQL is configured to start automatically at address 127.0.0.1, port 3306,
username root and blank password.

Example command to create a database:

```
mysql -u root -e 'create database test;'
```

Example command to load a SQL file and generate your schema:

```
mysql -u root -D test < schema.sql
```

## <a name="postgres"></a> Postgres

Postgres is configured to start automatically at address 127.0.0.1, port 5432,
username postgres and no password.

Example command to create a database:

```
psql -c 'create database test;' -U postgres
```

## <a name="mongodb"></a> MongoDB

Mongodb must be started manually, as part of your build script. You can
start Mongodb by executing the following command:

```
sudo start mongodb
sleep 10
```

## <a name="redis"></a> Redis

Redis must be started manually, as part of your build script. You can
start Redis by executing the following command:

```
sudo start redis
sleep 10
```

## <a name="memcache"></a> Memcache

Memcahce is configured to start automatically at address 127.0.0.1 and
port 11211 using default configurations.

## <a name="neo4j"></a> Neo4j

Neo4j must be started manually, as part of your build script. You can
start Neo4j by executing the following command:

```
neo4j start
sleep 5
```
## <a name="elasticsearch"></a> Elastic Search

Elastic Search must be started manually, as part of your build script. You can
start Elastic Search by executing the following command:

```
sudo start elasticsearch
sleep 5
```

## <a name="couchdb"></a> CouchDB

CouchDB must be started manually, as part of your build script. You can
start CouchDB by executing the following command:

```
sudo /etc/init.d/couchdb start
sleep 5
```
