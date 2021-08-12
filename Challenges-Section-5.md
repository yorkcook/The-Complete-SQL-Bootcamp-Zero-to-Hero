CHALLENGE FOR JOIN

Situation: Sales tax has changed in California. We need to get the emails for all customers in California to alert them of the change.

Solution:

SELECT district, email
FROM address
JOIN customer
ON address.address_id = customer.address_id
WHERE district = 'California'

Situation: A customer wants to know all the movies the actor Nick Wahlberg is in. Get a list of all the movies Nick Wahlberg is in.

Solution:

SELECT film.title, first_name, last_name
FROM actor
JOIN film_actor
ON actor.actor_id = film_actor.actor_id
JOIN film
ON film_actor.film_id = film.film_id
WHERE first_name = 'Nick' AND last_name = 'Wahlberg'
