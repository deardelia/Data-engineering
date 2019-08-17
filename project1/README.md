1.Description
The project aims to create a Postgres Database and an ETL pipline to optimize queries for song play analysis.

2.Database
the provided dataset is organized as .json form. we can call create_table.py to create tables from dataset.

3.Script introduction

create_tables.py : delete and created your table

etl.py: read and processes a single file from song_data and log_data and loads into your tables in ET

sql_queries.py : contains all sql queries.

4.Framework 

Create database -->  Design ETL(include reading json files and parse accordingly to store the tables into specific columns and proper formatting)