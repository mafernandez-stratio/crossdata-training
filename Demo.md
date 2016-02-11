* SELECT minute AS rangetime, sum_ta as total FROM shoppingcentertest.ci_minute_v1 ORDER BY sum_ta DESC LIMIT 10
* SELECT employee, SUM(total_amount) AS total_amount, SUM(total_products) AS total_products FROM ordershdfsdemo GROUP BY employee ORDER BY total_amount DESC LIMIT 5
* SELECT * FROM ordersdb.orderscoll WHERE shopping_center = 'Online' LIMIT 2
* SELECT id, first_name, email, gender, language, SUM(data.total_amount) AS totalamount FROM master.clients INNER JOIN ordersdb.orderscoll ON clients.id = orderscoll.client_id GROUP BY id, first_name, email, gender, languageORDER BY totalamount DESCLIMIT 5
* SELECT sc, channel, city, country, ts, sum_ta, sum_tp FROM ordershdfsdemo INNER JOIN shoppingcentertest.sc_ts_v1 ON ordershdfsdemo.shopping_center = sc_ts_v1.sc WHERE sum_tp > 1000LIMIT 4
* SELECT sss AS center, city, f AS section, ts, sum_tp AS total FROM ordersdb.orderscoll INNER JOIN shoppingcentertest.f_sss_ts_v1 ON f_sss_ts_v1.sss = orderscoll.shopping_centerWHERE sum_tp > 100 AND f = 'feeding'LIMIT 5
* SELECT name, postal_code, address, number_of_employees, SUM(total_products) AS tp FROM ordershdfsdemo INNER JOIN master.shopping_centers ON shopping_centers.name = ordershdfsdemo.shopping_centerWHERE day_time_zone = 'morning'GROUP BY name, postal_code, address, number_of_employeesORDER BY tp DESCLIMIT 5
* DROP TABLE crossdatatest.t1
* DROP TABLE crossdatatest.t2
* SHOW TABLES
* IMPORT TABLES USING com.stratio.crossdata.connector.cassandra OPTIONS (    cluster "Stratio Cluster",    keyspace "crossdatatest",    spark_cassandra_connection_host "capsaicina02.stratio.com
* SHOW TABLES
* DESCRIBE crossdatatest.t1


