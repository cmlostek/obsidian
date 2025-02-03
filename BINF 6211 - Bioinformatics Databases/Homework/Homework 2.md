1.List all projects with **project_id** between 10 and 100.
```SQL
SELECT * 
FROM project 
WHERE project_id BETWEEN 10 AND 100;
```

2.List all projects with the raw data size > 0.5GB.
```SQL
SELECT * 
FROM project 
WHERE raw_data_size_gb > 0.5;
```

3.List all projects with the raw data size > 0.5GB and **sequence_count** > 1000.
```sql
SELECT * 
FROM project 
WHERE raw_data_size_gb > 0.5 
  AND sequence_count > 1000;
```

4.List all projects with a name containing “COVID”
```sql
SELECT * 
FROM project 
WHERE name LIKE '%COVID%';
```

5.List all projects where the name or description contains “COVID”
```sql
SELECT * 
FROM project 
WHERE name LIKE '%COVID%' 
   OR description LIKE '%COVID%';
```

6.List all principal investigators with the last name “Smith”
```sql
SELECT * 
FROM principal_investigator 
WHERE last_name = 'Smith';
```

7.List all projects of all investigators with the last name “Smith”
```sql
SELECT p.* 
FROM project p
JOIN principal_investigator pi 
  ON p.principal_investigator_id = pi.principal_investigator_id
WHERE pi.last_name = 'Smith';
```

8.List all principal investigators whose project’s name or description contains “COVID”
```sql
SELECT DISTINCT pi.* 
FROM principal_investigator pi
JOIN project p 
  ON pi.principal_investigator_id = p.principal_investigator_id
WHERE p.name LIKE '%COVID%' 
   OR p.description LIKE '%COVID%';
```

9.Add a constraint for the **email** attribute to have values in the format “*@*” only.
```sql
ALTER TABLE principal_investigator
ADD CONSTRAINT email_format_check 
CHECK (email LIKE '%@%');
```

10.Write a query to count the number of projects for each principal investigator and assign that number to the attribute **project_count**.
```sql
UPDATE principal_investigator pi
SET project_count = (
    SELECT COUNT(*) 
    FROM project p 
    WHERE p.principal_investigator_id = pi.principal_investigator_id
);
```