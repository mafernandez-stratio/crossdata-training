IMPORT TABLES\n   USING com.stratio.crossdata.connector.mongodb\n   OPTIONS (\n   host 'capsaicina03.stratio.com:27017',\n   database 'ordersdb',\n   schema_samplingRatio '1.0'
IMPORT TABLES \nUSING com.stratio.crossdata.connector.cassandra \nOPTIONS (\n    cluster \"Stratio Cluster\",\n    spark_cassandra_connection_host \"capsaicina02.stratio.com
CREATE TABLE ordershdfsdemo USING org.apache.spark.sql.json OPTIONS (path \"hdfs://capsaicina05.stratio.com/user/stratio/ordershdfsdemo/*[^(tmp)]
SELECT * FROM ordershdfsdemo LIMIT 2
CREATE TABLE lineshdfsdemo USING org.apache.spark.sql.json OPTIONS (path \"hdfs://capsaicina05.stratio.com/user/stratio/lineshdfsdemo/*
SHOW TABLES
SELECT * FROM lineshdfsdemo LIMIT 5
SELECT * FROM ordershdfsdemo LIMIT 5
SELECT * FROM ordershdfsdemo WHERE shopping_center = 'Madrid' LIMIT 2
CREATE TABLE master.clients USING org.apache.spark.sql.jdbc OPTIONS (\n    url \"jdbc:postgresql://capsaicina01.stratio.com/master?user=crossdata&password=stratio\", \n    dbtable \"public.clients\", \n    driver \"org.postgresql.Driver
SELECT * FROM master.clients LIMIT 4
CREATE TABLE master.products USING org.apache.spark.sql.jdbc OPTIONS (\n    url \"jdbc:postgresql://capsaicina01.stratio.com/master?user=crossdata&password=stratio\", \n    dbtable \"public.products\", \n    driver \"org.postgresql.Driver
SELECT * FROM master.products LIMIT 4
CREATE TABLE master.shopping_centers USING org.apache.spark.sql.jdbc OPTIONS (\n    url \"jdbc:postgresql://capsaicina01.stratio.com/master?user=crossdata&password=stratio\", \n    dbtable \"public.shopping_centers\", \n    driver \"org.postgresql.Driver
SELECT * FROM master.shopping_centers LIMIT 4
SELECT * FROM ingestion.lines LIMIT 5
SHOW TABLES

