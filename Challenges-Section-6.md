CHALLENGES TIMESTAMPS

Situation:

During which months did payments occur? Format with full month name.

Solution:

SELECT DISTINCT(TO_CHAR(payment_date, 'MONTH'))
FROM payment

Situation:

How many payments occured on a Monday?

Solution:

SELECT COUNT(payment_date)
from payment
WHERE EXTRACT(dow FROM payment_date ) = 1
