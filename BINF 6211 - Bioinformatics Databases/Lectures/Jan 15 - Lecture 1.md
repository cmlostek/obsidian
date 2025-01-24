## Why Databases?
Databases provide a unified logical view of the data and hide the details of physical storage and access paths.

- If using a file system, updating a file individually may break the system, the program, and any tools dependent on the data within. 
- The unified logical view allows users to ignore all aspects of hardware and software details. 
	- This is important because a lot of different locations / labs are outputting the same data in different ways. Which means databases need to be able to handle the different formats of data. 
- Your database management system should be something that does not break when adding one column or one data point. 

## Characteristics of Databases
1. Ensure that data is complete and accessible without a high cost (rewriting applications)
2. Make data fields self documenting (human readable)
3. Limit data redundancy.
	1. Ideally each type of data exists in only one table in the database
4. Modularize the database to allow for *data independence*
	1. This just means that every query, every subset of a query, every function needs to be taken into account separately. Meaning you can change one portion of the data without affecting something else. 

A database logically consists of 3 layers:
- **A physical layer**
	- How the data is stored on a physical disk. *Physical Independence* is the ability to change the location of where a database is stored without affecting the ability for something to access to the data. 
	- Files, file system
- **Conceptual Layer** 
	- How the data is logically organized. *Logical independence* is the ability to change the conceptual scheme without changing the external views and programs. 
		- Logical independence is harder to achieve than physical independence
	- Schema, tables, relations
- **External View**
	- How the data is presented to the end-user
	- Web applications, html

## Database Design
We must clearly decide what the intended scope of the database content will be. Databases should be efficient, should solve redundancy of data, and should be secure. 
- What sources and types of data are available and from where
- What do users want to do with the data and who are those users
- What Hardware/OS and physical resources are available

## Database System Environment
The term *database system* refers to an organization of components that define and regulate the collection, storage, management, and use of data within a database environment


## Data Modeling for Database Design

### Data Model
- A simplified representation of the real world
- Different levels of complexity / detail will be specified in the conceptual and logical models and for schemas, and the physical models. 

### Model Building Blocks
- Entities
	- The nouns (A teacher, a student)
- Attributes
	- The adjectives or adverbs (A students grade, class)
- Relationships
	- The verbs (One teacher *teaches* 20 students)
		- These often depend on the direction you are reading from. Does not have to be symmetric. 
	One to Many (1 Sequence to Many proteins)
	One to One (one protein to one sequence)
	Many to Many (many chromosomes to many sequences)
- Constraints
	- Things that cannot be exceeded (Maximum number of students in a class)

## Organizing Data Elements

### Entities
- Entities often depend on the context of your database.

### Attributes

### Relationships

### Constraints
- These are restrictions placed on the data. Constraints are important because they help to ensure data integrity. 
- Constraints are often expressed in the form of rules.

## From the Reading
> [!PDF|note] [[ReadingAssignment_1.pdf#page=2&selection=13,30,14,49&color=note|manual describing standard operating procedures for curation to help maintain and communicate quality standards.]]
> 
> This is important so as to identify rules / guidelines for how information should be stored and interacted with within the database. 

