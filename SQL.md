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


