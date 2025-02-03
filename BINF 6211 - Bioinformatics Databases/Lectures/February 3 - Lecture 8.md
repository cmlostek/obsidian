## Joining Database Tables

SQL joins are the foundation of DBMS, enabling the combination of data from multiple tables based on relationships between columns. 

### Example:
![[Pasted image 20250203103119.png]]
``` SQL
SELECT s.roll_no, s.name, s.address, s.phone, s.age, sc.course_id
FROM Student s
JOIN StudentCourse sc ON sc.roll_no = sc.roll_no;
```
Hierarchy here allows for "s" and "sc" to be defined before we use them in the "SELECT" command. 


Inner Join selects all rows from both the tables as long as the condition is satisfied.
```SQL 
SELECT table1.column1, table1.column2, table2.column1,...
FROM table1
INNER JOIN table2
ON table1.matching_column = table2.matching_column;
```


LEFT JOIN returns all the rows of the table on the left side of the join and matches rows for the table on the right side of the join.
```SQL
SELECT table1.column1, table1.column2, table2.column1,...
FROM table1
LEFT JOIN table2
ON table1.matching_column = table2.matching_column;
```
![[Pasted image 20250203105327.png]]
Since there is no "6", "7", or "8" in the StudentCourse table then when using left join, you will return the null value for any value that is not matched up. 


Right join returns all the rows of the table on the right side of the join and matching rows for the table on the left side of the join.
```SQL 
SELECT table1.column1,table1.column2,table2.column1,.... 
FROM table1 
RIGHT JOIN table2 
ON table1.matching_column = table2.matching_column;
```


Full Join creates the result-set by combining results of both LEFT JOIN and RIGHT JOIN.
```SQL
SELECT table1.column1,table1.column2,table2.column1,.... 
FROM table1 
FULL JOIN table2 
ON table1.matching_column = table2.matching_column;
```

Returns a Cartesian product of both tables (every row from table A is paired with every row from table B).
```SQL
SELECT Musician.name, Album.album_name 
FROM Musician 
CROSS JOIN Album;
```