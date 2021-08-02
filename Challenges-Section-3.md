CHALLENGE GROUP BY

Situation 1: We want to give a bonus to the staffer who processed the most transactions. How many transactions did each staff member handle and who gets the bonus?

Solution:

SELECT staff_id, COUNT(payment_id)
FROM payment
GROUP BY staff_id

Situation 2: Corporate HQ is doing research to find out the avg replacement cost and movie rating. What is the avg replacement cost per rating?

Solution:

SELECT rating, ROUND(AVG(replacement_cost), 2)
FROM film
GROUP BY rating

Situation 3: We are running a promotion to reward our top 5 customers. What are the customer id number of the top 5 customers by total spend?

Solution:

SELECT customer_id, SUM(amount)
FROM payment
GROUP BY customer_id
ORDER BY SUM(amount) DESC
LIMIT 5

CHALLENGE HAVING

Situation 1: We are launching a reward program for our most loyal customers,these customers have 40 or more transactions. Which customer_ids are eligble for this new program?

Solution:

SELECT customer_id, COUNT(payment_id)
FROM payment
GROUP BY customer_id
HAVING COUNT(payment_id) >= 40

Situation 2: What are the customer_ids who have spent more than \$100 in payment transactions with staff_id number 2?

Solution:

SELECT customer_id, SUM(amount)
FROM payment
WHERE staff_id = 2
GROUP BY customer_id
HAVING SUM(amount) > 100
