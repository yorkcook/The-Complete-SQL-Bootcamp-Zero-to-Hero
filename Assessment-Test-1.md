Assessment Test 1

Situation 1: Return the customer_ids of the customers who have spent at least \$110 with the staff_id = 2.

Solution:

SELECT customer_id, SUM(amount)
FROM payment
WHERE staff_id = 2
GROUP BY customer_id
HAVING SUM(amount) >= 110

Situaton 2: How many films begin with the letter J?

Solution:

SELECT COUNT(title )
FROM film
WHERE title LIKE 'J%'

Situation 3: What customer has the highest customer_id whose name starts with E and an address_id lower than 500?

Solution:

SELECT first_name, last_name
FROM customer
WHERE first_name LIKE 'E%' and address_id < 500
ORDER BY customer_id DESC
LIMIT 1
