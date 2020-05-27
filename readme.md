the Q's
--table person

Create a table called person that records a person's id, name, age, height ( in cm ), city, favorite_color.
id should be an auto-incrementing id/primary key - Use type: SERIAL
Add 5 different people into the person database.
Remember to not include the person_id because it should auto-increment.
List all the people in the person table by height from tallest to shortest.
List all the people in the person table by height from shortest to tallest.
List all the people in the person table by age from oldest to youngest.
List all the people in the person table older than age 20.
List all the people in the person table that are exactly 18.
List all the people in the person table that are less than 20 and older than 30.
List all the people in the person table that are not 27 (Use not equals).
List all the people in the person table where their favorite color is not red.
List all the people in the person table where their favorite color is not red and is not blue.
List all the people in the person table where their favorite color is orange or green.
List all the people in the person table where their favorite color is orange, green or blue (use IN).
List all the people in the person table where their favorite color is yellow or purple (use IN).

--make person table

-- create table person (
-- 	person_id serial,
--   person_name varchar(30),
--   person_age int,
--   height float(2),
--   city varchar(35),
--   favorite_color varchar(15)
-- );

--adding people

-- insert into person (
-- 	person_name,
--   person_age,
--   height,
--   city,
--   favorite_color
-- ) values (
--   'Jason Towner',
--   26,
--   198,
--   'Phoenix',
--   'Orange' 
-- );
-- insert into person (
-- 	person_name,
--   person_age,
--   height,
--   city,
--   favorite_color
-- ) values (
--   'Cole Towner',
--   15,
--   182,
--   'Phoenix',
--   'Green' 
-- );
-- insert into person (
-- 	person_name,
--   person_age,
--   height,
--   city,
--   favorite_color
-- ) values (
--   'Barrett Smith',
--   30,
--   146,
--   'Estes Park',
--   'Blue' 
-- );
-- insert into person (
-- 	person_name,
--   person_age,
--   height,
--   city,
--   favorite_color
-- ) values (
--   'Drew Wilcocks',
--   26,
--   154,
--   'Fort collins',
--   'purple' 
-- );
-- insert into person (
-- 	person_name,
--   person_age,
--   height,
--   city,
--   favorite_color
-- ) values (
--   'Dylan Hicks',
--   26,
--   186,
--   'phoenix',
--   'red' 
-- );

-- sort tallest to smallest
-- select * from person
-- order by height desc

-- sort smallest to tallest
-- select * from person 
-- order by height asc

-- sort by age
-- select * from person 
-- order by person_age desc;

-- list all over 20
-- select * from person
-- where person_age >= 20;

--list age === 18
-- select * from person
-- where person_age = 18;

-- older then 30 younger then 20
-- select * from person 
-- where person_age <20
-- and person_age <30;

--not age 27 using !=
-- select * from person
-- where person_age != 27;

-- fav color is not red
-- select * from person
-- where favorite_color != 'red';

--fav color is not red or blue
-- select * from person
-- where favorite_color != 'red'
-- and favorite_color !='Blue';

-- fav color is green or orange
-- select * from person 
-- where favorite_color = 'Orange'
-- or favorite_color = 'Green';

-- fav color is orange, green, blue use in
-- select * from person 
-- where favorite_color in ('Orange', 'Blue', 'Green')

-- fav color is yellow or purple
-- select * from person
-- where favorite_color in ('yellow', 'purple');

--Table orders
Create a table called orders that records: order_id, person_id, product_name, product_price, quantity.
Add 5 orders to the orders table.
Make orders for at least two different people.
person_id should be different for different people.
Select all the records from the orders table.
Calculate the total number of products ordered.
Calculate the total order price.
Calculate the total order price by a single person_id.

-- -- make orders table
-- create table orders(
-- 	order_id serial,
--   person_id varchar(30),
--   product_name varchar(30),
--   product_price float(2),
--   quantity int
-- );

-- make 5 orders
-- insert into orders(
-- 	person_id,
--   product_name,
--   product_price,
--   quantity
-- )values(
-- 	'funny guy',
--   'glasses',
--   10.00,
--   1
-- );
-- insert into orders(
-- 	person_id,
--   product_name,
--   product_price,
--   quantity
-- )values(
-- 	'funny guy',
--   'glasses',
--   10,
--   5
-- );
-- insert into orders(
-- 	person_id,
--   product_name,
--   product_price,
--   quantity
-- )values(
-- 	'buff guy',
--   'tank top',
--   15,
--   1
-- );
-- insert into orders(
-- 	person_id,
--   product_name,
--   product_price,
--   quantity
-- )values(
-- 	'buff guy',
--   'tank top',
--   15,
--   3
-- );
-- insert into orders(
-- 	person_id,
--   product_name,
--   product_price,
--   quantity
-- )values(
-- 	'computer guy',
--   'headphones',
--   100,
--   1
-- );

-- select all
-- select * from orders

-- total number of orders
-- select count(order_id) from orders

-- sum of price
-- select sum (product_price * quantity) from orders

-- total sum of order by one person
-- select sum(product_price * quantity) from orders
-- where person_id = 'computer guy'


Add 3 new artists to the artist table. ( It's already created )
Select 10 artists in reverse alphabetical order.
Select 5 artists in alphabetical order.
Select all artists that start with the word 'Black'.
Select all artists that contain the word 'Black'.

-- select * from artist

-- add fleetwood mac and the black keys as well
-- insert into artist(
-- 	name
-- ) values (
--   'flight of the conchords'
-- );

-- first ten in reverse alphabetical order
-- select * from artist 
-- order by name desc limit 10

-- five in alphabetical order
-- select * from artist 
-- order by name asc limit 5

-- first word starts with Black
-- select * from artist
-- where name like 'Black%';

-- select * from artist
-- where name like '%Black%';

Q's
List all employee first and last names only that live in Calgary.
Find the birthdate for the youngest employee.
Find the birthdate for the oldest employee.
Find everyone that reports to Nancy Edwards (Use the ReportsTo column).
You will need to query the employee table to find the Id for Nancy Edwards
Count how many people live in Lethbridge.

-- select all that live in calgary
-- select * from employee
-- where city = 'Calgary';

-- get youngest employee
-- select max(birth_date) from employee; 

--get oldest employee
-- select min(birth_date) from employee;

-- reports to nancy
-- select * from employee
-- where reports_to = 1;

-- live in lethbridge
-- select count(*) from employee
-- where city = 'Lethbridge';


Count how many orders were made from the USA.
Find the largest order total amount.
Find the smallest order total amount.
Find all orders bigger than $5.
Count how many orders were smaller than $5.
Count how many orders were in CA, TX, or AZ (use IN).
Get the average total of the orders.
Get the total sum of the orders.

-- total from USA
-- select count(*) from invoice
-- where billing_country = 'USA'

--largest order 
-- select max(total) from invoice;
-- select * from invoice

-- get min total
-- select min(total) from invoice

-- total is larger then 5
-- select * from invoice 
-- where total > 5;

-- sum of totals smaller then 5
-- select count(*) from invoice 
-- where total < 6;

-- orders in ca tx or az
-- select * from invoice
-- where billing_state in ('CA', 'TX', 'AZ');

--avg total
-- select avg(total) from invoice

-- get sum of orders
-- select sum(total) from invoice
