# sqlhomeworkfirst
pluorositenotes and table homework 
Databases collect and organize data to allow for easy retrieval. All our devices use databases.
Table holds data that would be used in a data base and allows for it to be easily retrieved.
Row represents an entire data record within a table.
Columns describes the type of data in it.
SELECT statement is needed to get movie information. E.g 
SELECT title
FROM movies;

To select more than one,
SELECT id, title, genre, duration
FROM movies;

To select and return everything, 
SELECT  *
FROM movies;
ALL sequel statements must have a semi column at the end to close.
WHERE clause can be used to filter out data and match the requested data. It filters out other information and will return only the match that is requested.
SELECT title
FROM movies
WHERE id = 2;

Searching for a string of data;
SELECT  *
FROM movies
WHERE title = ‘the Kid’;

Sorting data
The ORDER BY  clause can be used to sort data in a specific way.
SELECT title
FROM movies
ORDER BY duration;  //from shortest to longest duration time OR from ascending order.
ORDER BY duration DESC; from descending order, longest to shortest duration time.

SELECT title
FROM movies
WHERE duration > 100;

<> is the not equal to sign.
SELECT title
FROM movies
WHERE genre <> ‘Horror’ ;  //its saying where genre is not equal to horror.


Using AND operator to filter multiple conditions.
SELECT title
FROM movies
WHERE id = 1
AND genre = ‘Comedy’;
PS. All conditions of the SELECT statement must be met. If not, by search or query, will return no records, as shown. BOTH the WHERE and AND conditions must both be true.

 Instead of AND, what if we want either or?
OR operator can be used to filter multiple conditions.
SELECT title
FROM movies
WHERE id = 1
OR genre = ‘Comedy’

ADDING data to the current table
To add information to an existing table, we use the INSERT statement.
INSERT INTO  movies (id, title, genre, duration)
VALUES (5, ‘The Circus’, ‘Comedy’, 71);

Another way to add data to a table is demonstrated below. 

INSERT INTO movies
VALUES (5, ‘The Circus’, ‘Comedy’, 71);

Changing the data using SQL
We want to change the genre for the fil “The Circus” from a Comedy to a Romance;
To change the movie data, UPDATE statement is needed.
Update RECIPE
UPDATE movies
SET genre = ‘Romance”
WHERE id = 5;
We can use OR to perform multiple updates/changes.

Deleting/Removing data
In order to remove data from an existing table, we wou;d have to use the DELETE statement.
DELETE FROM movies WHERE id = 5;
 Removing multiple data = DELETE FROM movies WHERE id < 100;
 
Managing Databases and tables; 




mysql> insert into movies(id, title, genre, duration)
    -> values(1, 'Metropolis', 'Sci-Fi', 153);
Query OK, 1 row affected (0.19 sec)

mysql> select * from movies;
+----+------------+--------+----------+
| id | title      | genre  | duration |
+----+------------+--------+----------+
|  1 | Metropolis | Sci-Fi |      153 |
+----+------------+--------+----------+
1 row in set (0.01 sec)

mysql> insert into movies
    -> values(2, 'Nosferatu', 'Horror', 94);
Query OK, 1 row affected (0.00 sec)

mysql> select * from movies;
+----+------------+--------+----------+
| id | title      | genre  | duration |
+----+------------+--------+----------+
|  1 | Metropolis | Sci-Fi |      153 |
|  2 | Nosferatu  | Horror |       94 |
+----+------------+--------+----------+
2 rows in set (0.00 sec)

mysql> insert into movies
    -> values(3, 'The Kid', 'Comedy', 68);
Query OK, 1 row affected (0.01 sec)

mysql> select * from movies;
+----+------------+--------+----------+
| id | title      | genre  | duration |
+----+------------+--------+----------+
|  1 | Metropolis | Sci-Fi |      153 |
|  2 | Nosferatu  | Horror |       94 |
|  3 | The Kid    | Comedy |       68 |
+----+------------+--------+----------+
3 rows in set (0.00 sec)

mysql> insert into movies
    -> values(4, 'The Gold Rush', 'Adventure', 95);
Query OK, 1 row affected (0.00 sec)

mysql> select * from movies;
+----+---------------+-----------+----------+
| id | title         | genre     | duration |
+----+---------------+-----------+----------+
|  1 | Metropolis    | Sci-Fi    |      153 |
|  2 | Nosferatu     | Horror    |       94 |
|  3 | The Kid       | Comedy    |       68 |
|  4 | The Gold Rush | Adventure |       95 |
+----+---------------+-----------+----------+
4 rows in set (0.00 sec)

mysql> select title from movies;
+---------------+
| title         |
+---------------+
| Metropolis    |
| Nosferatu     |
| The Kid       |
| The Gold Rush |
+---------------+
4 rows in set (0.00 sec)

mysql> select title from movies where id = 2;
+-----------+
| title     |
+-----------+
| Nosferatu |
+-----------+
1 row in set (0.02 sec)

mysql> 
