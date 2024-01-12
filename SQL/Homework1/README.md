# Homework1
Bu ödevde [PostgreSQL](https://www.postgresqltutorial.com/) Tutorial sayfasındaki [örnek veritabanı](https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/) kullanılmıştır.
Örnek veritabanını indirmek için [tıklayınız](https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip).
------
## Örnek1
film tablosunda bulunan 'title' ve 'description' sütunlarındaki verileri sıralayınız.
Sorgu : 
SELECT title, description FROM public.film
ORDER BY film_id ASC
------
## Örnek2
film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.
Sorgu : 
SELECT * FROM public.film
WHERE length BETWEEN 60 AND 75
ORDER BY film_id ASC
-----
## Örnek3
film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
Sorgu : 
SELECT * FROM public.film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99)
ORDER BY film_id ASC
-----
## Örnek4
customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
Sorgu : 
SELECT last_name FROM public.customer
WHERE first_name = 'Mary'
ORDER BY customer_id ASC
-----
## Örnek5
film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
Sorgu : 
SELECT * FROM public.film
WHERE NOT length > 50 AND NOT (rental_rate = 2.99 OR rental_rate = 4.99)
ORDER BY film_id ASC