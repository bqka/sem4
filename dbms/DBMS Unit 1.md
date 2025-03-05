![[Pasted image 20250302071821.png]]
![[Pasted image 20250302071848.png]]

A Database is a structured collection of inter-related data, facilitating easy access, management and updates.

![[Pasted image 20250302071856.png]]
![[Pasted image 20250302071908.png]]

Characteristics of DBMS
![[Pasted image 20250305081606.png]]

Database Schema
![[Pasted image 20250305081638.png|400]]

**Instance**: set of values of a relation at a particular moment

![[Pasted image 20250305025450.png]]

**Schema**: collection of schemas of all the relations of that database. illustrates the logical structure and organization of data

![[Pasted image 20250305025502.png]]

![[Pasted image 20250305025606.png]]

# Data Independence

![[Pasted image 20250305081918.png]]
![[Pasted image 20250305081928.png]]
# Data Abstraction

view of database
- **physical level** - details about data storage, access on hardware, data types
- **logical level** - Above the physical level, this level showcases data as entity sets and their relationships, detailing the types and connections between stored data in the database.
- **view level** - displaying only a portion of the entire database focusing on user-interest areas. It can represent multiple views of the same data, allowing users to access information through various applications from the database

![[Pasted image 20250305081449.png|300]]
# Keys

Attributes/Collection of attributes that can uniquely identify a tuple

**Super Key:** A **Super Key** is a set of one or more attributes that uniquely identify a tuple (row) in a relation. It can have extra attributes that are not necessary for uniqueness.
![[Pasted image 20250305030350.png|400]]

**Candidate Key:** A **Candidate Key** is a minimal Super Key—meaning no attributes can be removed without losing uniqueness.
![[Pasted image 20250305030405.png|400]]

**Primary Key:** A **Primary Key** uniquely identifies each record in a table.

**Foreign Key**: A **Foreign Key** is an attribute that establishes a relationship between tables.

**Partial Key:** A key that is not a primary key by itself but if combined with the primary key of a strong entity set, acts as a primary key.

**Search Key:** A **Search Key** is an attribute or a set of attributes used to retrieve records from a database efficiently. It is primarily used in indexing to improve the performance of search operations.
# Entity Relationship Diagram

**Entity** ![[Pasted image 20250305030834.png]]

![[Pasted image 20250305030905.png]]

**Entity Set:** Collection of same type of entities that share the same properties/attributes.

**Attributes:** are the units that define and describe properties and characteristics of entities.

**Strong Entity Set:** has a primary key

**Weak Entity Set:** does not have a primary key and needs to be connected to a strong entity set

![[Pasted image 20250305031209.png]]

# Specialization

![[Pasted image 20250305082528.png]]

# Generalization

- total or partial
- overlapping or disjoint

![[Pasted image 20250305082608.png]]

# Conversion of ER Diagram to Relations

every relation needs 
- name
- schema
- primary key

1. Create a new relation for every strong entity set
2. create new relation for weak entity sets with PK = PK of strong entity set + partial key
3. create a new relation for every relationship set
	 - schema of this relation -> all primary keys/relations it is connected to
	 ![[Pasted image 20250305082935.png|500]]
4. ignore all identifying relationship sets as relation obtained will be redundant with weak entity set
5. Multivalued attribute - with name same as the MVA, primary key as the (PK of relation/entity set it is connected to + this attribute) - the PK is union of 2
![[Pasted image 20250305083124.png|400]]

![[Pasted image 20250305083250.png]]