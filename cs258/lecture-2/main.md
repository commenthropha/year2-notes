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
```sql
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
```sql
CREATE SCHEMA <schemaName>;
```

Or, assigning a new owner:
```sql
CREATE SCHEMA <schemaName> AUTHORIZATION '<ownerUsername>';
```

Whenever you create a schema, it is added to the [[Database Schema|database schema/catalog]]
#### `DROP`
To drop (delete) a table:
```sql
DROP TABLE <tableName>;
```

To drop (delete) a schema:
```sql
DROP schematist <schemaName>;
```
### SQL as a DML
Other than basic retrieval queries, there are a number of other interesting and meaningful things that we can do with SQL when utilising it as a DML
#### `VIEW`s
We can create a view in the following manner:
```sql
CREATE VIEW seventies_albums AS 
SELECT * FROM albums 
WHERE release_date BETWEEN ... AND ...;
```
#### `PROCEDURE`s and `FUNCTION`s
- We can modify databases within a `PROCEDURE`
- We can only perform queries within a `FUNCTION`
```sql
CREATE OR REPLACE FUNCTION trigger_new_artist() 
	RETURNS TRIGGER 
	LANGUAGE PLPGSQL 
AS $$ 
BEGIN 
	INSERT INTO artists VALUES (NEW.artist) ON CONFLICT DO NOTHING; 
	RETURN NEW; 
END; 
$$;
```
#### `TRIGGER`s
A trigger is a procedure which runs when a certain event, such as a database insertion or deletion, occurs
```sql
CREATE TRIGGER new_album_highlight 
ON albums AFTER INSERT 
AS 
INSERT INTO new_albums VALUES (NEW.name);
```
#### Common Table Expressions (CTEs)
Common Table Expressions are temporary results defined with the WITH keyword that can be used as part of a larger query
```sql
WITH
	x AS ..., 
	y AS ..., 
SELECT ...;
```