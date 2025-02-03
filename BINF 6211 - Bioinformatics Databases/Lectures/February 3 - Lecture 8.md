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

```SQL 
SELECT table1.column1, table1.column2, table2.column1,...
FROM table1
INNER JOIN table2
ON table1.matching_column = table2.matching_column;
```

```SQL
SELECT table1.column1, table1.column2, table2.column1,...
FROM table1
LEFT JOIN table2
ON table1.matching_column = table2.matching_column;
```