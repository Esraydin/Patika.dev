1-film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

`SELECT COUNT(*) FROM film where length > ( SELECT AVG(length) from film );`

2-film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

`SELECT COUNT(*) from film where MAX(rental_rate) = ( SELECT MAX(rental_rate) from film );`

3-film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

`SELECT * FROM film WHERE 
MIN(rental_rate) = ALL (SELECT * FROM film WHERE MIN(rental_rate))
AND replacement_cost = ALL
(SELECT * FROM film WHERE MIN(replacement_cost));`

4-payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

`SELECT payment.customer_id, customer.fist_name, customer.last_name, COUNT(customer.payment_id)
FROM payment
INNER JOIN customer
ON customer.customer_id = payment.customer_id;
GROUP BY customer.customer_id, customer.last_name, customer.last_name
ORDER BY COUNT(payment.customer_id) DESC;`
