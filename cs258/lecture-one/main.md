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
### Formal Definition
Informally, a relation is a **table** of values having a set of rows and columns