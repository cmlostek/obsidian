
## Data Definition Language (DDL)

- ALTER TABLE gene MODIFY (organism integer);
	- changes the type to integer
- ALTER TABLE gene ADD (organism_id integer);
	- adds the column organism_id to the table gene
- ALTER TABLE gene DROP COLUMN organism_id;
	- removes the column organism_id to the table gene
- ALTER TABLE gene RENAME TO not_gene;
	- renames the table gene


## Data Manipulation Language (DML)

Adding rows (records) to an existing table

INSERT INTO tablename (col1, col2, col3, ...)
VALUES (value1, value2, value3, ...)


