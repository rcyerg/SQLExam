# SQLExam

1.
INSERT INTO movies (Title, Runtime, Genre, IMDB_Score, Rating) VALUES
('Avatar', 180, 'Fantasy', 8.5, 'PG'),
('Dark Knight Rises', 120, 'Action', 7.8, 'PG-13');

2.
SELECT *
FROM movies
WHERE Genre='Sci-Fi';

3.
SELECT *
FROM movies
 WHERE IMDB_Score >= 6.5;

4.
SELECT *
FROM movies
WHERE Rating IN ('PG', 'G') AND Runtime <= 100;

5.
SELECT Genre, AVG(Runtime) AS 'AvgRuntime under 7.5 IMDB'
FROM movies
WHERE IMDB_SCORE <= 7.5 GROUP BY Genre;

6.
UPDATE movies
SET Rating='R'
WHERE Title='Starship Troopers';

7a.
ALTER TABLE movies
DROP PRIMARY KEY,
ADD id INT NOT NULL PRIMARY KEY AUTO_INCREMENT;

7b.
SELECT Title, IMDB_Score, Rating
FROM movies
WHERE Genre IN ('Horror', 'Documentary');

8.
SELECT Rating, AVG(IMDB_Score), MIN(IMDB_Score), MAX(IMDB_Score)
FROM movies
GROUP BY Rating;

9.
SELECT Rating, COUNT(* ) AS '# of Movies', AVG(IMDB_Score), MIN(IMDB_Score), MAX(IMDB_Score)
FROM movies
GROUP BY Rating
HAVING COUNT(*) > 1;

10.
DELETE
FROM movies
WHERE Rating='R';

11.
DROP TABLE movies;

12.
DROP DATABASE movies_db;






