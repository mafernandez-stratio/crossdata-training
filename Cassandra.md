* DROP KEYSPACE crossdatatest;
* DESCRIBE KEYSPACES;
* CREATE KEYSPACE crossdatatest WITH REPLICATION = { \n\t'class' : 'org.apache.cassandra.locator.SimpleStrategy', \n\t'replication_factor': '1' }\nAND DURABLE_WRITES = true;
* CREATE TABLE crossdatatest.t1(id INT PRIMARY KEY, user VARCHAR);
* CREATE TABLE crossdatatest.t2(name VARCHAR PRIMARY KEY, total INT);
* SELECT * FROM ingestion.lines WHERE lucene = '{ filter: {type: \"fuzzy\", field: \"product\", value: \"strops\"} }' LIMIT 2;
