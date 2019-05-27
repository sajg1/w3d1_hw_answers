
QUESTION 1
------------------
 SELECT * FROM movies;
```
 psql -d marvel -f marvel.sql


  id |                title                | year | show_time
 ----+-------------------------------------+------+-----------
   1 | Iron Man                            | 2008 | 15:10
   2 | The Incredible Hulk                 | 2008 | 20:45
   3 | Iron Man 2                          | 2010 | 13:15
   4 | Thor                                | 2011 | 18:55
   5 | Captain America: The First Avenger  | 2011 | 22:50
   6 | Avengers Assemble                   | 2012 | 12:35
   7 | Iron Man 3                          | 2013 | 15:35
   8 | Thor: The Dark World                | 2013 | 15:55
   9 | Batman Begins                       | 2005 | 15:40
  10 | Captain America: The Winter Soldier | 2014 | 21:00
  11 | Guardians of the Galaxy             | 2014 | 23:40
  12 | Avengers: Age of Ultron             | 2015 | 21:25
  13 | Ant-Man                             | 2015 | 23:40
  14 | Captain America: Civil War          | 2016 | 15:15
  15 | Doctor Strange                      | 2016 | 22:35
  16 | Guardians of the Galaxy 2           | 2017 | 15:55
  17 | Spider-Man: Homecoming              | 2017 | 17:40
  18 | Thor: Ragnarok                      | 2017 | 15:55
  19 | Black Panther                       | 2018 | 17:45
  20 | Avengers: Infinity War              | 2018 | 14:50
 (20 rows)
```
 QUESTION 2
---------------
 SELECT name FROM people;
```
 psql -d marvel -f marvel.sql

 name        

George Gordon
Stephen Gossip
Simon Hall
Katherine Kerr
John McNeill
Shae Nicholsun
Rory O'Shea
Jamie Paterson
Harrison Booth
Stephanie Scullion
Patryk Smacki
Robert Tam
Michal Tyranski
Michael Urquhart
Kyle Walker
Jeremy Wood
(16 rows)
```
QUESTION 3
----------------
UPDATE people SET name = 'Chae Nicholson' WHERE name = 'Shae Nicholsun';

SELECT * FROM people WHERE name = 'Chae Nicholson';
```
psql -d marvel -f marvel.sql

id |      name      
----+----------------
  6 | Chae Nicholson
(1 row)
```
QUESTION 4
-----------------
SELECT name FROM people WHERE name = 'Stephen Gossip';
```
psql -d marvel -f marvel.sql

name      

Stephen Gossip
(1 row)
```
QUESTION 5
----------------
DELETE FROM movies WHERE title = 'Batman Begins';
SELECT title FROM movies WHERE title = 'Batman Begins';
```
psql -d marvel -f marvel.sql

DELETE 1
 title

(0 rows)
```
QUESTION 6
---------------
INSERT INTO people (name) VALUES ('Louise Camlin');
SELECT * FROM people WHERE name = 'Louise Camlin';
```
psql -d marvel -f marvel.sql

id |     name      
----+---------------
 17 | Louise Camlin
(1 row)
```
QUESTION 7
----------------
DELETE FROM people WHERE name = 'Harrison Booth';
SELECT * FROM people WHERE name = 'Harrison Booth';
```
psql -d marvel -f marvel.sql

DELETE 1
 id | name
----+------
(0 rows)
```
QUESTION 8
---------------
INSERT INTO movies (title, year, show_time) VALUES ('Captain Marvel', 2019, '00:00');
SELECT * FROM movies WHERE title = 'Captain Marvel';
```
psql -d marvel -f marvel.sql

INSERT 0 1
 id |     title      | year | show_time
----+----------------+------+-----------
 21 | Captain Marvel | 2019 | 00:00
(1 row)
```
QUESTION 9
----------------
SELECT show_time FROM movies WHERE title = 'Guardians of the Galaxy';
UPDATE movies SET show_time = '01:40' WHERE title = 'Guardians of the Galaxy 2';
SELECT * FROM movies WHERE title = 'Guardians of the Galaxy 2';
```
psql -d marvel -f marvel.sql

show_time

 23:40
(1 row)

UPDATE 1
 id |           title           | year | show_time
----+---------------------------+------+-----------
 16 | Guardians of the Galaxy 2 | 2017 | 01:40
(1 row)
```
Extensions
----------------
DELETE FROM people WHERE name = 'Stephen Gossip' OR name = 'Harrison Booth';
SELECT * FROM people;
```
psql -d marvel -f marvel.sql

DELETE 2
 id |        name        
----+--------------------
  1 | George Gordon
  3 | Simon Hall
  4 | Katherine Kerr
  5 | John McNeill
  6 | Shae Nicholsun
  7 | Rory O'Shea
  8 | Jamie Paterson
 10 | Stephanie Scullion
 11 | Patryk Smacki
 12 | Robert Tam
 13 | Michal Tyranski
 14 | Michael Urquhart
 15 | Kyle Walker
 16 | Jeremy Wood
(14 rows)
```
