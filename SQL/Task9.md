1-city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

`SELECT city, country FROM country
INNER JOIN city on country.country_id = city.city_id;`

2-customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.


`SELECT payment.payment_id, customer.first_name, customer.last_name FROM customer
INNER JOIN payment on payment.payment_id = customer.customer_id;`

3-customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

`SELECT rental.rental_id, customer.first_name, customer.last_name FROM customer
INNER JOIN rental on rental.rental_id = customer.customer_id;`
