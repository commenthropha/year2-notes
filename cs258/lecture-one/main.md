# Introduction to Database Systems
### Principle Functions
In a nutshell, DB systems provide software to 'manage' data:
1. **Model** data
2. **Access** data (query and update)
3. **Analyse** data (complex queries)
4. **Store** data
5. **Secure** data
6. [[Ensure Data Consistency|Ensure data consistency]]
7. [[Optimise Data Accesses|Optimise data accesses]]

### Thinking of Database Systems (as a black box)
We can think of a Database System as a "box" with a nice interface offering the above functionality that is based on:
- an easy to understand data model
- a [[declarative programming language]] (e.g. SQL)

A framework commonly used to describe the *structure* of a database system is the [[3 Schema DBMS Architecture]] model.
### Key Facts about Data
- Modern data is extremely large (reaching petabytes of data) and too large to fit in memory
	- Consequently, contemporary data is typically decentralised

- Data is either structured or unstructured (web pages, text docs)
	- Databases are designed with **structured data** in mind
 
# The Relational Model
## Informal Definition
A database can be described as *a set of structured data stored in a computer*. Relational databases are an extension of that concept based on a relational model of data storage. 

In this model, databases are comprised of **tables** (also called [[Relation||relations]]), which themselves consist of **rows** (also called [[Tuple|tuples]]) and **columns** which represent an individual characteristic/attribute of interest of that entity

The structure or shape of the data in the table is called the **table schema**. The set of tables schemas in a database is called the **database schema**.
## Formal Definitions
- [[Tuple]]
- [[Relation]]
- [[Domain]]
- [[Relation State]]
## Keys
Keys encode the concept of unique identification in Relational Databases

A [[superkey]] uniquely identifies a tuple in a relation
We can extend this idea to define a [[candidate key]]

We use *primary keys* to uniquely identify rows in a relation. While any [[superkey]] would be valid, using a [[candidate key]] is a simpler and more sensible approach
## Constraints
These narrow the set of valid/permissible values that an attribute can take from the domain. There are several notable types:

| Constraint| Description | 
| -------- | -------- |
| Entity Integrity | Primary Keys cannot be `NULL` | 
| Domain | Limit the domain of an attribute (`NOT NULL` on a key field can be considered a domain constraint) |
| Referential Integrity | Foreign Keys cannot refer to non-existent rows. |
| Semantic Attribute Integrity | Semantic constraints such as non-negative limit on a bank balance column |
| Functional Dependencies | Describe relationships between columns (see next section) |
## Functional Dependencies
These establish a functional relationship between two sets of attributes based on the real-world relationships between those attributes.

The expression X -> Y, read as "Y depends on X" is a [[Functional Dependency]], defined as follows:
