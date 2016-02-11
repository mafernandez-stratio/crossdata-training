* DROP KEYSPACE crossdatatest;
* DESCRIBE KEYSPACES;
* CREATE KEYSPACE crossdatatest WITH REPLICATION = { 'class' : 'org.apache.cassandra.locator.SimpleStrategy', 'replication_factor': '1' }AND DURABLE_WRITES = true;
* CREATE TABLE crossdatatest.t1(id INT PRIMARY KEY, user VARCHAR);
* CREATE TABLE crossdatatest.t2(name VARCHAR PRIMARY KEY, total INT);
* SELECT * FROM ingestion.lines WHERE lucene = '{ filter: {type: "fuzzy", field: "product", value: "strops"} }' LIMIT 2;
* 
