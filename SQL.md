## Ödev 1: 

#### 1
~~~sql
SELECT title, description FROM film;
~~~  
#### 2
~~~sql
SELECT * FROM film WHERE length > 60 AND length < 75;
~~~

3
~~~sql
SELECT * FROM film WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
~~~
4
~~~sql
SELECT * FROM customer WHERE first_name = 'Mary';
~~~
5
~~~sql
SELECT * FROM film WHERE length < 50 AND NOT (rental_rate = 4.99 OR rental_rate = 2.99) 
~~~

## Ödev 2 :

#### 1
~~~sql
SELECT * FROM film WHERE replacement_cost BETWEEN 14.99 AND 16.99
~~~


#### 2
~~~sql
SELECT first_name,last_name FROM actor WHERE first_name IN ('Penelope','Nick','Ed')
~~~


#### 3
~~~sql
SELECT * FROM film WHERE rental_rate IN (0.99,2.99,4.99) AND replacement_cost IN (12.99,15.99,28.99)
~~~

## Ödev 3 :


#### 1
~~~sql
SELECT * FROM country WHERE country LIKE 'A%a'
~~~

#### 2
~~~sql
SELECT * FROM country WHERE country LIKE '______%n' 
~~~


#### 3
~~~sql
SELECT * FROM film WHERE title ILIKE '%t%t%t%t%';
~~~

#### 4
~~~sql
SELECT * from film WHERE title Like 'C%' AND length>90 AND rental_rate=2.99
~~~


## Ödev 4 :

#### 1 
~~~sql
SELECT DISTINCT replacement_cost FROM film
~~~

#### 2
~~~sql
SELECT COUNT(DISTINCT replacement_cost) FROM film
~~~

#### 3

~~~sql
SELECT COUNT(*) from film WHERE title LIKE 'T%' AND rating='G'
~~~

#### 4

~~~sql
SELECT COUNT(*) from country WHERE country LIKE '_____'
~~~



#### 5

~~~sql
SELECT COUNT(*) from city WHERE city LIKE '%r'
~~~


## Ödev 5 


#### 1

~~~sql
SELECT * from film WHERE title LIKE '%n' ORDER BY length DESC LIMIT 5
~~~

#### 2

~~~sql
SELECT * from film WHERE title LIKE '%n' ORDER BY length ASC LIMIT 5 OFFSET 5
~~~

#### 3
~~~sql
SELECT * FROM Customer WHERE store_id=1  ORDER BY last_name DESC LIMIT 4
~~~

## Ödev 6

#### 1
~~~sql
SELECT AVG(rental_rate) FROM film 
~~~

#### 2
~~~sql
SELECT COUNT(*) FROM film  WHERE title LIKE 'C%'
~~~


#### 3
~~~sql
SELECT Max(length) FROM film WHERE  rental_rate=0.99 
~~~

#### 4
~~~sql
SELECT COUNT(DISTINCT replacement_cost) FROM film WHERE length>150
~~~

## Ödev 7

#### 1
~~~sql
SELECT rating from film GROUP BY rating
~~~

#### 2
~~~sql
SELECT COUNT(replacement_cost),replacement_cost from film GROUP BY replacement_cost HAVING COUNT(replacement_cost)>50
~~~


#### 3
~~~sql
SELECT store_id,Count(store_id) FROM customer GROUP By store_id
~~~

#### 4
~~~sql
SELECT COUNT(country_id) ,country_id FROM city  GROUP BY country_id ORDER BY COUNT (country_id) DESC LIMIT 1
~~~

## Ödev 8 



#### 1
~~~sql

CREATE TABLE employee(
	id serial PRIMARY KEY,
	name VARCHAR (50),
	birthday DATE,
	email VARCHAR ( 100 )
);

~~~

#### 2
~~~sql

insert into employee (id, name, birthday, email) values (1, 'Krysta Cirlos', '03/10/1991', 'kcirlos0@goo.ne.jp');
insert into employee (id, name, birthday, email) values (2, 'Lorettalorna Mulcaster', '09/08/1999', 'lmulcaster1@gmpg.org');
insert into employee (id, name, birthday, email) values (3, 'Lazare Jeffry', '09/09/1998', 'ljeffry2@i2i.jp');
insert into employee (id, name, birthday, email) values (4, 'Dian Lightwood', '14/03/1994', 'dlightwood3@ucoz.com');
insert into employee (id, name, birthday, email) values (5, 'Nicola Govey', '05/06/1992', 'ngovey4@ucsd.edu');
insert into employee (id, name, birthday, email) values (6, 'Dorthy Dugget', '28/11/1991', 'ddugget5@creativecommons.org');
insert into employee (id, name, birthday, email) values (7, 'Jaclin Rate', '26/07/1996', 'jrate6@youtube.com');
insert into employee (id, name, birthday, email) values (8, 'Brier Brimble', '06/10/1996', 'bbrimble7@icio.us');
insert into employee (id, name, birthday, email) values (9, 'Base Thorwarth', '30/03/2000', 'bthorwarth8@sciencedirect.com');
insert into employee (id, name, birthday, email) values (10, 'Eve McDonell', '22/10/1999', 'emcdonell9@bigcartel.com');
insert into employee (id, name, birthday, email) values (11, 'Lyndsie Ridley', '30/10/1992', 'lridleya@google.nl');
insert into employee (id, name, birthday, email) values (12, 'Gabriele Yakutin', '11/06/1996', 'gyakutinb@netscape.com');
insert into employee (id, name, birthday, email) values (13, 'Teddi Bullough', '21/10/1999', 'tbulloughc@dell.com');
insert into employee (id, name, birthday, email) values (14, 'Matty Danniel', '20/01/1996', 'mdannield@usa.gov');
insert into employee (id, name, birthday, email) values (15, 'Prue Portsmouth', '23/06/1994', 'pportsmouthe@blogs.com');
insert into employee (id, name, birthday, email) values (16, 'Ripley Blanning', '12/08/1999', 'rblanningf@springer.com');
insert into employee (id, name, birthday, email) values (17, 'Francoise Lintall', '30/06/1992', 'flintallg@spiegel.de');
insert into employee (id, name, birthday, email) values (18, 'Carole MacClinton', '20/02/1993', 'cmacclintonh@google.com.au');
insert into employee (id, name, birthday, email) values (19, 'Marietta Felton', '03/04/1996', 'mfeltoni@unc.edu');
insert into employee (id, name, birthday, email) values (20, 'Hally Stickney', '26/08/1990', 'hstickneyj@mozilla.org');
insert into employee (id, name, birthday, email) values (21, 'Felicia Jaslem', '24/12/1995', 'fjaslemk@statcounter.com');
insert into employee (id, name, birthday, email) values (22, 'Ira Toor', '19/01/1994', 'itoorl@cbslocal.com');
insert into employee (id, name, birthday, email) values (23, 'Roseline Reinard', '16/04/1993', 'rreinardm@tmall.com');
insert into employee (id, name, birthday, email) values (24, 'Noam Bear', '05/08/1997', 'nbearn@sohu.com');
insert into employee (id, name, birthday, email) values (25, 'Gordy Orta', '07/01/1992', 'gortao@cam.ac.uk');
insert into employee (id, name, birthday, email) values (26, 'Alysa Dullingham', '02/04/1992', 'adullinghamp@bluehost.com');
insert into employee (id, name, birthday, email) values (27, 'Gertrudis Sabban', '14/08/1993', 'gsabbanq@creativecommons.org');
insert into employee (id, name, birthday, email) values (28, 'Henri Handforth', '04/12/1999', 'hhandforthr@cyberchimps.com');
insert into employee (id, name, birthday, email) values (29, 'Konstanze Van den Dael', '08/08/1991', 'kvans@engadget.com');
insert into employee (id, name, birthday, email) values (30, 'Maegan Learmonth', '03/12/1991', 'mlearmontht@google.nl');
insert into employee (id, name, birthday, email) values (31, 'Bryanty Gookey', '08/10/2000', 'bgookeyu@foxnews.com');
insert into employee (id, name, birthday, email) values (32, 'Blair Setchell', '02/05/1997', 'bsetchellv@cornell.edu');
insert into employee (id, name, birthday, email) values (33, 'Scarface Morfell', '16/07/1999', 'smorfellw@gravatar.com');
insert into employee (id, name, birthday, email) values (34, 'Yankee Peabody', '02/05/1991', 'ypeabodyx@ted.com');
insert into employee (id, name, birthday, email) values (35, 'Herbert Piddocke', '12/01/1991', 'hpiddockey@cocolog-nifty.com');
insert into employee (id, name, birthday, email) values (36, 'Sallyann Maggill''Andreis', '14/05/1995', 'smaggillandreisz@smh.com.au');
insert into employee (id, name, birthday, email) values (37, 'Damita Brigg', '25/12/1998', 'dbrigg10@squarespace.com');
insert into employee (id, name, birthday, email) values (38, 'Kattie Dowrey', '11/10/1997', 'kdowrey11@slashdot.org');
insert into employee (id, name, birthday, email) values (39, 'Wernher Wolseley', '22/03/2000', 'wwolseley12@paypal.com');
insert into employee (id, name, birthday, email) values (40, 'Keeley Bumfrey', '06/06/1993', 'kbumfrey13@prweb.com');
insert into employee (id, name, birthday, email) values (41, 'Dukie McQuirk', '15/09/1992', 'dmcquirk14@ucoz.com');
insert into employee (id, name, birthday, email) values (42, 'Piggy Doick', '29/08/1992', 'pdoick15@vistaprint.com');
insert into employee (id, name, birthday, email) values (43, 'Krystle Chapman', '17/02/1990', 'kchapman16@vistaprint.com');
insert into employee (id, name, birthday, email) values (44, 'Jonis Bouch', '20/01/2000', 'jbouch17@harvard.edu');
insert into employee (id, name, birthday, email) values (45, 'Batholomew Duffrie', '26/04/1992', 'bduffrie18@abc.net.au');
insert into employee (id, name, birthday, email) values (46, 'Sigismund Groarty', '26/03/1998', 'sgroarty19@jigsy.com');
insert into employee (id, name, birthday, email) values (47, 'Ariana Philippe', '07/03/1990', 'aphilippe1a@ucoz.com');
insert into employee (id, name, birthday, email) values (48, 'Ruddie Poluzzi', '08/05/1991', 'rpoluzzi1b@php.net');
insert into employee (id, name, birthday, email) values (49, 'Monique Fildery', '07/02/1995', 'mfildery1c@tiny.cc');
insert into employee (id, name, birthday, email) values (50, 'Justinian Hassekl', '22/08/1996', 'jhassekl1d@pinterest.com');
~~~


#### 3
~~~sql
UPDATE employee SET name='Spam ACCOUNT' WHERE email LIKE '%ucoz.com'
UPDATE employee SET name='Lazare Sherrif' WHERE Id=3 
UPDATE employee SET email='user@employee.com'  WHERE birthday BETWEEN '1996/01/01' AND '2000/01/01'
~~~

#### 4
~~~sql

DELETE FROM employee WHERE WHERE email LIKE '%ucoz.com'
DELETE FROM employee WHERE Id='3'
DELETE FROM employee WHERE birthday BETWEEN '1996/01/01' AND '2000/01/01'
~~~

## Ödev 9

#### 1
~~~sql
SELECT city.city,country.country from  city INNER JOIN country ON city.country_id= country.country_id
~~~

#### 2
~~~sql
SELECT customer.first_name,customer.last_name,payment.payment_id from  payment INNER JOIN customer ON payment.customer_id=customer.customer_id
~~~

#### 3
~~~sql
SELECT customer.first_name,customer.last_name,rental.rental_id from  rental INNER JOIN customer ON rental.customer_id=customer.customer_id
~~~


## Ödev 10 

#### 1
~~~sql
SELECT city.city,country.country from  city LEFT JOIN country ON city.country_id= country.country_id
~~~

#### 2
~~~sql
SELECT customer.first_name,customer.last_name,payment.payment_id from  payment RIGHT JOIN customer ON payment.customer_id=customer.customer_id
~~~

#### 3
~~~sql
SELECT customer.first_name,customer.last_name,rental.rental_id from  rental FULL JOIN customer ON rental.customer_id=customer.customer_id
~~~


## Ödev 11 

#### 1
~~~sql
(SELECT first_name FROM customer) UNION ALL (SELECT first_name FROM customer)
~~~

#### 2
~~~sql
 (SELECT first_name FROM customer) INTERSECT  (SELECT first_name FROM customer)
~~~

#### 3
~~~sql
(SELECT first_name FROM customer) UNION  (SELECT first_name FROM customer)
~~~

#### 4
~~~sql
  (SELECT first_name FROM customer) UNION ALL (SELECT first_name FROM customer)
  (SELECT first_name FROM customer) INTERSECT ALL  (SELECT first_name FROM customer)
  (SELECT first_name FROM customer) UNION ALL  (SELECT first_name FROM customer)
~~~





