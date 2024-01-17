# Homework9

Bu ödevde [PostgreSQL](https://www.postgresqltutorial.com/) Tutorial sayfasındaki [örnek veritabanı](https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/) kullanılmıştır.
Örnek veritabanını indirmek için [tıklayınız](https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip).

------

## Örnek1

city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

Sorgu : 

**SELECT city, public.country.country**

**FROM public.city**

**INNER JOIN public.country ON city.country_id = public.country.country_id**

**ORDER BY city.city**

![Github](assets/answer1.png)

-----

## Örnek2

customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

Sorgu : 

**SELECT payment.payment_id, customer.first_name, customer.last_name**

**FROM customer**

**INNER JOIN payment ON customer.customer_id = payment.customer_id**

![Github](assets/answer2.png)

-----

## Örnek3

customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

Sorgu : 

**SELECT rental.rental_id, customer.first_name, customer.last_name**

**FROM customer**

**INNER JOIN rental ON customer.customer_id = rental.customer_id**

![Github](assets/answer3.png)