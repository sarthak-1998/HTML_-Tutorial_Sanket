SHOW DATABASES;
// to show all the databases available on your system. 

USE <database name>;
// to select a particular database to run queries on

SHOW TABLES;
// To list down all the tables of a particular selected database

CREATE DATABASE <name>;
// to create a new database

CREATE TABLE <name> { 
   <column name 1> [datatype] <keyword>,
   <column name 2> [datatype],
   .
   .

};
// to create a new table 

DESC <table name>;
// show structure and description of the table


INSERT INTO <table name> (col1, col2, ....) VALUES (<value 1>, <value 2>, ...)
// to insert values into a table 

SELECT <column name> FROM <table name>;
// to get a specific column data from a table
// use * in place of column name to get all the columns.


//("Sanket","2022-01-02","Male"),("Neha","2019-03-04","Female"),("King","1999-01-04","Other"),("JD","2020-01-03","Male"),("Sanket","2022-01-06","Male"),("Neha 2","2019-07-04","Female"),("Kingg","1999-01-04","Other"),("JD","2020-01-03","Male")


SELECT * FROM <table name> WHERE {coditions ..}

Conditions -> comparisson of column data with your values

Example - SELECT * FROM second WHERE DoB > '2000-01-01' AND Gender = 'Female';

SELECT * FROM second ORDER BY DoB DESC;
 SELECT * FROM second WHERE NOT Gender = 'Male';
  SELECT * FROM second WHERE DoB > '2020-01-03' OR Gender = 'Female';
  SELECT * FROM second WHERE Name LIKE "_a%";
  SELECT * FROM second WHERE Name LIKE "%a%";

  SELECT * FROM second WHERE Gender = 'Female' ORDER BY DoB DESC LIMIT 2;   