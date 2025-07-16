wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0110EN-SkillsNetwork/datasets/sakila/sakila_mysql_dump.sql

mysql --host=mysql --port=3306 --user=root --password

create database sakila;

use sakila;

source sakila_mysql_dump.sql;

SHOW FULL TABLES WHERE table_type = 'BASE TABLE';

DESCRIBE staff;

SELECT * FROM staff;

\q

mysqldump --host=mysql --port=3306 --user=root --password sakila staff > sakila_staff_mysql_dump.sql

cat sakila_staff_mysql_dump.sql
