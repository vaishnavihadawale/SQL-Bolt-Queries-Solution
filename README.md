# SQL-Bolt-Queries-Solution 
# Lesson 1
Q1 Find the title of each film
Select Title from Movies;

Q2 Find the director of each film
Select Director from Movies;

Q3 Find the title and director of each film
Select Title, Director from Movies

Q4 Find the Title and Year of each film
Select Title, Year from Movies

Q5 Find all information about each film
Select * from Movies

# Lesson 2
Q1 Find the movie with a row id of 6
select * from Movies where id=6;

Q2 Find the movies released in the years between 2000 and 2010 
select * from Movies where year between 2000 and 2010;

Q3 Find the movies not released in the years between 2000 and 2010 
select * from Movies where year not in between 2000 and 2010;

Q4 Find the first 5 Pixar movies and their release year
SELECT * FROM movies limit 5;

# Lesson 3
Q1 Find all the Toy Story movies
SELECT * FROM movies where Title like 'Toy Story%';

Q2 Find all the movies directed by John Lasseter
SELECT Title FROM movies where Director='John Lasseter';

Q3 Find all the movies (and director) not directed by John Lasseter 
SELECT Title FROM movies where Director!='John Lasseter';

Q4 Find all the WALL-* movies 
Select * from Movies where Title like 'Wall-%';





