DELETE FROM <table name> WHERE {comparisson ..} ORDER BY .. LIMIT .. ;

 DELETE FROM Names  WHERE name LIKE "%e%" ORDER BY name LIMIT 1;
 DELETE FROM Names;



UPDATE <table name> SET <column 1> = value 1 WHERE {conditions};

UPDATE Actors SET FirstName = "RJ", NetWorthInMillions = 1000 WHERE Id = 6;


ALTER TABLE  <table name> CHANGE  <old column name> <new column name> [new constraint (datatype or constraint)]

ALTER TABLE Actors CHANGE NetWorthInMillions NetWorth DECIMAL(10,2);


ALTER TABLE <table name> ADD <column name> [parameters - datatype and constraint]

ALTER TABLE Actors DROP MiddleName ;
ALTER TABLE Actors ADD MiddleName VARCHAR(10) AFTER FirstName;
ALTER TABLE Actors CHANGE Region Speciality VARCHAR(20);

SELECT DoB AS "Date of Birth" FROM Actors;
SELECT CONCAT(FirstName,' ' ,SecondName) AS Name FROM Actors;

SELECT SUM(NetWorth) FROM Actors;
SELECT SUM(Score) FROM students2 WHERE Marital_Status = 'Married';
 SELECT AVG(Score) FROM students2 WHERE Marital_Status = 'Married';
 SELECT AVG(Score) FROM students2 WHERE Marital_Status = 'Single';
  SELECT COUNT(*) AS "No. of Single People"  FROM Students2 WHERE Marital_Status = 'Single';
SELECT DISTINCT Score FROM students2;




SELECT Marital_Status, Count(*) FROM students2 GROUP BY Marital_Status ;
SELECT Name FROM Students2 GROUP BY Name ORDER BY Name;

SELECT DOB, Count(*) FROM Students2 GROUP BY DOB HAVING DOB > '1998-04-26' ;
 



