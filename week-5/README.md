# Databases Week 5

## Main Topics

* Database Indexing
    - [Relational Database Internals (Arabic - عربي) (TechVault)](https://www.youtube.com/playlist?list=PLE8kQVoC67PzGwMMsSk3C8MvfAqcYjusF) [5:8]

* SQL Transactions
    - [44 Transactions in SQL Server (Ahmed Samir El Khadrawy)](https://www.youtube.com/watch?v=aqxav5cFMMM)

## Extra Resources

* Database Indexing
    - [21. Database Indexing: How DBMS Indexing done to improve search query performance? Explained (Shrayansh)](https://www.youtube.com/watch?v=6ZquiVH8AGU)

* SQL Transactions
    - [Transactions in SQL (HowTech)](https://www.youtube.com/watch?v=PhUgUTutiGk)

## Task (30 pts.)

* Explain how to create an index in SQL Server. **(3 pts.)**

* What are the cases where using transactions is needed? and why is the transaction statement usually wrapped inside a `TRY/CATCH` block? **(3 pts.)**

* Explain how SQL transactions apply ACID principles. **(3 pts.)**

* _(From Instabug Internship Assesment)_ Assume we have a table called sales with columns (id, rental_date, inventory_id, customer_id) and the table has a clustered innoDB index on id (primary key) and a B+ tree index on (rental_date, inventory_id). A clustered index in innoDB contains the entire row (all columns) in its leaf nodes while a B+ tree index in innoDB contains only the indexed columns (rental_date, inventory_id) and the primary key (id) in its leaf node. How many index lookups (index access) will each of the following queries perform? **(10 pts.)**
    1. ```sql
        SELECT * FROM sales WHERE id = 5;
        ```
    2. ```sql
        SELECT * FROM sales WHERE rental_date = "2021-01-01";
        ```
    3. ```sql
        SELECT inventory_id FROM sales WHERE rental_date = "2021-01-01";
        ```
    4. ```sql
        SELECT rental_date FROM sales WHERE inventory_id = 126;
        ```
    5. ```sql
        SELECT * FROM sales WHERE inventory_id = 126 and rental_date = "2021-01-01";
        ```

* Solve [ITI Lab 6](https://docs.google.com/document/d/1inqB0MJaxEB1sl4NepLqiSTzmeOlZjyT/view). **(11 pts.)**