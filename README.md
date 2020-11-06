# project-1
/* Create table about the people and what they do here */
CREATE TABLE Movie_stars (id INTEGER PRIMARY KEY , name TEXT,Country TEXT ); 
INSERT INTO Movie_stars VALUES (1, "Ahmad helmy", "egypt");
INSERT INTO Movie_stars VALUES (2, "Mona zaki", "egypt");
INSERT INTO Movie_stars VALUES (3, "Solaf fwakhrji", "syria");
INSERT INTO Movie_stars VALUES (4, "Wael ramadan", "syria");
INSERT INTO Movie_stars VALUES (5, "Amr yousef", "egypt");
INSERT INTO Movie_stars VALUES (6, "kinda alloush", "syria");
INSERT INTO Movie_stars VALUES (7, "asser yassin", "egypt");
CREATE TABLE Movies (id INTEGER PRIMARY KEY , Movie TEXT,Year INTEGER);
INSERT INTO Movies VALUES (1, "keda reda", 2007);
INSERT INTO Movies VALUES (2, "africano", 2001);
INSERT INTO Movies VALUES (3, "haleem", 2006);
INSERT INTO Movies VALUES (4, "share' shekagho", 2020);
INSERT INTO Movies VALUES (5, "hepta", 2016);
INSERT INTO Movies VALUES (6, "brtita", 2012);
INSERT INTO Movies VALUES (7, "diamond dust", 2018);
CREATE TABLE coubles (id INTEGER PRIMARY KEY , id1_coubles INTEGER,id2_coubles INTEGER);
INSERT INTO coubles (id1_coubles,id2_coubles) VALUES (1,2); 
INSERT INTO coubles (id1_coubles,id2_coubles) VALUES (3,4); 
INSERT INTO coubles (id1_coubles,id2_coubles) VALUES (5,6);
INSERT INTO coubles (id1_coubles,id2_coubles) VALUES (7,"NULL");

SELECT Movie_stars.id,Movie_stars.name,Movies.Movie FROM Movie_stars
JOIN Movies
ON Movie_stars.id=Movies.id;


SELECT a.name,b.name as partner FROM coubles
JOIN Movie_stars a
ON coubles.id1_coubles=a.id
LEFT OUTER JOIN Movie_stars b
ON coubles.id2_coubles=b.id;
