# SQL - Structured Query Language
## SQL as a Language
SQL is a [[year2-notes/cs258/lecture-1/Declarative Programming Language|Declarative Programming Language]]

This removes a great deal of complexity from data manipulation as the underlying DB implementation is responsible for finding the optimal way to retrieve the required data

SQL is both:
- a [[Data Definition Language]] (DDL)
- a [[Data Manipulation Language]] (DPL)
### SQL as a DDL
#### `CREATE TABLE`
Tables are created by specifying a name, type and (optionally) constraints for each column, comma separated within parentheses: 
```
CREATE TABLE students ( 
	studentID INTEGER PRIMARY KEY, 
	studentName CHAR VARYING(30), 
	courseID INTEGER 
);
```
#### More on Constraints
##### Attribute Constraints
###### `NOT NULL`
- Specifies that NULL is not permitted
###### `DEFAULT`
- Specifies the default value of an attribute
- `DEFAULT <value>`
###### `CHECK`
- Allows attribute constraints based on application semantics
- `CHECK (condition)`
#### `CREATE SCHEMA`
We can create a new [[table schema]] as follows:
```
CREATE SCHEMA <schemaName>;
```
Or, assigning a new owner:
```
CREATE SCHEMA <schemaName> AUTHORIZATION '<ownerUsername>';
```

Whenever you create a schema, it is added to the [[Database Schema|database schema/catalog]]
#### `DROP`
To drop (delete) a table:
```
DROP TABLE <tableName>;
```
