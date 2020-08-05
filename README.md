Readme
=======
This library help you to copy your data(Table wise) from Oracle Database to Postgresql Database.



>Following librarys are use :
```sh
import pandas as pd
import numpy as np
import cx_Oracle
from sqlalchemy import create_engine
```
Connection Details
---------------------------
> **Note:** All credentials of Database connection should me correct.

Have to provide all credentials for the connection like User name , password and Host etc. for both the database and also provide table name which you want to copy from Oracle DB to Postgresql DB, after providing all credentials get pandas dataframe having table name and count of rows in table as output .

How to use code
-----------------------
Import orc2pstgrs library 
```sh
import orc2pstgrs
```
After getting the orc2pstgrs library ,then create connection with Oracle DB 
```sh
dataload.oracleDBconnection(host_name,port,service_name,user_name,password_orc)
```
Create connection with PostgreSQL DB
```sh
dataload.postgresDBconnection(user,password,host,port_pos,database_name)
```
Now, ETL start here by just giving the table name
```sh
dataload.TableDetails(table_name_of_orcle,table_name_use_to_save_in)
```
OR use SQL query to Extract table
```sh
dataload.GettablewithSQL(query,table_name_use_to_save_in)
```


> **Note:** Libraries like **cx_Oracle** and **sqlalchemy** are very powerful so can be use  alone for ETL job.