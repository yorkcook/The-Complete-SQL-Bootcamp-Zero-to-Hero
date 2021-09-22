CHALLENGE FOR SELECT

Situation: Send out promotional email to customers.

Solution: SELECT first_name, last_name, email FROM customer;

---

CHALLENGE FOR SELECT DISTINCT

Situation: We have a visitor from Australia who is unfamiliar with movie ratings in the USA. We want to know what are the movie ratings we have in our database.

Solution: SELECT DISTINCT(rating) FROM film

---

CHALLENGES FOR SELECT WHERE

Situation: A customer forgot their wallet at the store. We need to find the email for Nancy Thomas.

Solution:

SELECT email
FROM customer
WHERE first_name = 'Nancy' AND last_name = 'Thomas'

Situation: A customer wants to know the description for the movie "Outlaw Hanky".

Solution:

SELECT description
FROM film
WHERE title ='Outlaw Hanky'

Situation: We have the address for a customer who has been mailed a late notice. But we want to give them a call also. What is their phone number?

---

CHALLENGE ORDER BY

Situation: We want to reward the first 10 paying customers and need their customer id number.

Solution:

SELECT customer_id
FROM payment
ORDER BY payment_date ASC
LIMIT 10

Situation: A customer wants to watch a movie over their lunch break. What are the 5 shortest movies by run time.

SOLUTION:

SELECT title
FROM film
ORDER BY length ASC
LIMIT 5

Situation: IF previous customer has 50 minutes to watch a movie, how many total movies could they pick from?

SOLUTION:

SELECT COUNT(\*)
FROM film
WHERE length <= 50

---

GENERAL CHALLENGE 1

Situation 1: How many payment transactions were greater than \$5?

Solution:

SELECT COUNT(\*)
FROM payment
WHERE amount > 5

Situation 2: How many actors have a first name that starts with P?

Solution:

SELECT COUNT(\*)
FROM actor
WHERE first_name LIKE 'P%'

Situation 3: How many unique districts are our customers from?

Solution:

SELECT COUNT(DISTINCT(district))
FROM address

Situation 4: Retrieve list of names for the distinct districts from the previous question.

Solution:

SELECT DISTINCT(district)
FROM address

Situation 5: How many films have a rating of R and a replacement cost between 5 and 15?

Solution:

SELECT COUNT(\*)
FROM film
WHERE rating = 'R'
AND replacement_cost BETWEEN 5 AND 15

Situation 6: How many films have the word Truman in the title?

Solution:

SELECT COUNT(\*)
FROM film
WHERE title LIKE '%Truman%'
