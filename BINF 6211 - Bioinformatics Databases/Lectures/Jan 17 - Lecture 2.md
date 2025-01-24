# Entity Relationship Models

## Theoretical Basis of the Entity Relationship Model
- Based on Set Theory
- Has fully developed and coherent algebra defining operations
- A standardized application exists for a high level, declarative query

Each entity (table) is considered a set of records.

Conceptual modeling is the first stage of the design process. 


### Chen Style
- A rectangle represents an entity set.
- An oval represents the attributes
- A diamond represents a relationship. Connectivity is written next to each entity box. 
	- Read the connectivity on the side closer to the ending entity.
- While not always, the Chen model can include arrows to show the direction of the intended relationship

> [!NOTE] Note!
> Things can tend to get crowded here if you have a lot of attributes
> Add a * to the attributes you think are is a key (unique) identifier. 

#### Extended Example
##### Some Recommended Rules
- Names are **not** capitalized
- Avoid spaces and special symbols in names
- Use an * or highlight to indicate values likely to be unique

### Crows Foot
- A rectangle represents an entity
- The entity name is in the top portion
- The attributes re listed in the bottom section, in a column below the line. 
- Mark keys as PK (Primary Key) and FK (Foreign Key).
- Relationships are represented by lines.
	- the *ring* represents *zero* (0)
		- 0| is *zero or one*
		- >0 is *zero or many*
	- the *dash* represents *one* (|)
		- || is *one and only one*
		- >| is *one or many*
	- the *crows foot* represents *many* or *infinite* (< or >)
