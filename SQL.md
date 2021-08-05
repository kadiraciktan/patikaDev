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





