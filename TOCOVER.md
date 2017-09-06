# Topics to Cover

This is a list of topics that will be covered in today's lecture.

## What is a relational database? 
- like an excel sheet
- columns, rows and keys
- different sql languages
  - we are using postgreSQL

## Schemas 

- blueprint for your database
- instructions for how to set up your table

CREATE TABLE <table name> (
  <column name> <data type> [<constraint>],
  <column name> <data type> [<constraint>] ...
);

## Datatypes

- Null 
- Numeric
  - INTEGER - round number
  - DECIMAL - unlimited decimal places
  - FLOAT - 15 decimal places
  - SERIAL (incrementing integer) usually used with primary keys
- Character
  - TEXT - unlimited characters
  - VARCHAR(n) - limited characters

## SQL statement 

- AKA Query
- Semi-colons
- no trailing commas

## SELECTS

- SELECT *
  FROM <table name>
- SELECT <column name> [, <column name...>]
  FROM <table name>;
- WHERE Clause
  - Comparison operators 
    - >, <, >=, !=, etc....
  - Logical operators
    - AND, OR
  - IS NULL, IS NOT NULL (cannot do = NULL or != NULL)
  - <column name> IN(<list of values>) (short syntax for multiple ORs)
    - can also use NOT IN()
  - BETWEEN <value> AND <another value> (shorthand for multiple comparison operators like < >)
- LIMIT <number> 
  - limit returned rows
- ORDER BY <column name> DESC or ASC;
- Aggregate functions
  - min(), max(), sum(), avg(), count()
  - Count does not take into account null values
- <column name> LIKE '%something here%'
- Case insensitive 
  - SQL Syntax
  - Column names
  - Like partials
 - DISTINCT 
  - returns no duplicate values


## Adding, Updating, Removing Rows in a Table

- INSERT INTO <table name>
  (<column names...>)
  VALUES
  (<values matching the column order>);

- UPDATE <table name>
  SET <column name> = <new value>
  WHERE id = <id number>

- DELETE FROM <table name>
  WHERE id = <id number>
    - DO NOT FORGET WHERE CLAUSE
    - Practice with select statement first
    
- DROP TABLE <table name>;
