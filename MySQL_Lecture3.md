Joins??

Right, Left, Inner and Outer Join + Self Join

SELECT * FROM <table 1> INNER JOIN <table 2> ON {join condition}

 SELECT * FROM Actors INNER JOIN DigitalAssets ON Actors.Id = DigitalAssets.Id ;

 SELECT * FROM Actors LEFT JOIN DigitalAssets ON Actors.Id = DigitalAssets.Id ;

 SELECT * FROM Actors RIGHT JOIN DigitalAssets ON Actors.Id = DigitalAssets.Id ;

 SELECT * From Actors, DigitalAssets WHERE Actors.Id=DigitalAssets.Id;
 // for same as inner join 


 SELECT FirstName, DoB, URL FROM Actors LEFT JOIN DigitalAssets USING(Id);
 SELECT FirstName, DoB, URL FROM Actors RIGHT JOIN DigitalAssets USING(Id);
SELECT FirstName, DoB, URL FROM DigitalAssets RIGHT JOIN Actors USING(Id); // same result as the 1st query as tables postions are changed

// USING(id) only when both tables have same connecting column name


SELECT Firstname, DoB,URL FROM Actors INNER JOIN DigitalAssets; 
// Cartesian Product i.e every row from table a matched with every other row from table b - Count is No. of rows of A * No. of rows of B


(SELECT * FROM students2) UNION (SELECT * FROM tempactors);
//UNION of query results i.e just mergeing both query results into 1 output - only when column count is same.



SELF JOIN 

Table -  id, employee name, x, y, z, manager id