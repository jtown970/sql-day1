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