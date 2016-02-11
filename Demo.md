* SELECT minute AS rangetime, sum_ta as total FROM shoppingcentertest.ci_minute_v1 ORDER BY sum_ta DESC LIMIT 10
* SELECT employee, SUM(total_amount) AS total_amount, SUM(total_products) AS total_products FROM ordershdfsdemo \nGROUP BY employee \nORDER BY total_amount DESC LIMIT 5
* SELECT * FROM ordersdb.orderscoll WHERE shopping_center = 'Online' LIMIT 2
* SELECT id, first_name, email, gender, language, SUM(data.total_amount) AS totalamount FROM master.clients \nINNER JOIN ordersdb.orderscoll ON clients.id = orderscoll.client_id \nGROUP BY id, first_name, email, gender, language\nORDER BY totalamount DESC\nLIMIT 5
* SELECT sc, channel, city, country, ts, sum_ta, sum_tp FROM ordershdfsdemo \nINNER JOIN shoppingcentertest.sc_ts_v1 ON ordershdfsdemo.shopping_center = sc_ts_v1.sc \nWHERE sum_tp > 1000\nLIMIT 4
* SELECT sss AS center, city, f AS section, ts, sum_tp AS total FROM ordersdb.orderscoll \nINNER JOIN shoppingcentertest.f_sss_ts_v1 ON f_sss_ts_v1.sss = orderscoll.shopping_center\nWHERE sum_tp > 100 AND f = 'feeding'\nLIMIT 5
* SELECT name, postal_code, address, number_of_employees, SUM(total_products) AS tp FROM ordershdfsdemo \nINNER JOIN master.shopping_centers ON shopping_centers.name = ordershdfsdemo.shopping_center\nWHERE day_time_zone = 'morning'\nGROUP BY name, postal_code, address, number_of_employees\nORDER BY tp DESC\nLIMIT 5
* DROP TABLE crossdatatest.t1
* DROP TABLE crossdatatest.t2
* SHOW TABLES
* IMPORT TABLES \nUSING com.stratio.crossdata.connector.cassandra \nOPTIONS (\n    cluster \"Stratio Cluster\",\n    keyspace \"crossdatatest\",\n    spark_cassandra_connection_host \"capsaicina02.stratio.com
* SHOW TABLES
* DESCRIBE crossdatatest.t1

