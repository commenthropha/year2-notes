The three-schema architecture breaks the database down into three levels. Starting from the innermost level, these are:
1. [[Inner Level]]
2. [[Conceptual Level]]
3. [[External Level]]

These levels don't exist independently of each other; there is [[Mapping Between Views]] to enable correspondence between the three types of schema.
### Advantages
The separation offered by the 3 Schema DBMS Architecture is desirable as:
- Different users need different views of the same data.
- The approach in which a particular user needs to see the data may change over time.
- The users of the database should not worry about the physical implementation and internal workings of the database such as data compression and encryption techniques, hashing, optimization of the internal structures etc.
