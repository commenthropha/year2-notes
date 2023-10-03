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