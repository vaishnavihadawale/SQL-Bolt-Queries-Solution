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

Select * FROM movies limit 5;

# Lesson 3
Q1 Find all the Toy Story movies

SELECT * FROM movies where Title like 'Toy Story%';

Q2 Find all the movies directed by John Lasseter

SELECT Title FROM movies where Director='John Lasseter';

Q3 Find all the movies (and director) not directed by John Lasseter 

SELECT Title FROM movies where Director!='John Lasseter';

Q4 Find all the WALL-* movies 

Select * from Movies where Title like 'Wall-%';

# Lesson 4

Q1 List all directors of Pixar movies (alphabetically), without duplicates 

SELECT Distinct Director FROM Movies order by director asc;

Q2 List the last four Pixar movies released (ordered from most recent to least) 

SELECT * FROM Movies order by Year desc limit 4 ;

Q3 List the first five Pixar movies sorted alphabetically

SELECT Title  FROM Movies order by Title asc limit 5 ;

Q4 List the next five Pixar movies sorted alphabetically 

SELECT Title  FROM Movies order by Title asc limit 5 offset 5 ;

# Lesson 5

Q1 Find the domestic and international sales for each movie 

SELECT title, domestic_sales, international_sales FROM movies JOIN boxoffice ON movies.id = boxoffice.movie_id;

Q2 Show the sales numbers for each movie that did better internationally rather than domestically

SELECT id,title,  international_sales FROM movies JOIN boxoffice ON movies.id = boxoffice.movie_id where international_sales>domestic_sales;

Q3 List all the movies by their ratings in descending order

SELECT title,rating from movies join boxoffice on movies.id = boxoffice.movie_id order by rating desc;

# Lesson 6

Q1 Find the list of all buildings that have employees 

Select distinct building from employees;

Q2 Find the list of all buildings and their capacity

Select building_name, capacity from Buildings;

Q3 List all buildings and the distinct employee roles in each building (including empty buildings)

Select distinct building_name, role from Buildings left join Employees on buildings.building_name=employee.building ;


# Lesson 7

Q1 Find the name and role of all employees who have not been assigned to a building

SELECT role ,name FROM employees where building is null;

Q2 Find the names of the buildings that hold no employees 

SELECT  building_nameFROM buildings LEFT JOIN employees ON building_name = building WHERE name IS NULL;




