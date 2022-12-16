# Patika.dev SQL Dersi Odev 10


## 1. city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.

**Cozum:**

```SQL
SELECT city, country FROM city
LEFT JOIN country ON city.country_id = country.country_id;
```

**Sonuc:**

![Sonuc](/images/SqlOdev10_1.jpg)


## 2. customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.

**Cozum:**

```SQL
SELECT payment_id, first_name, last_name FROM customer
RIGHT JOIN payment ON customer.customer_id = payment.customer_id;
```

**Sonuc:**

![Sonuc](/images/SqlOdev10_2.jpg)



## 3. customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.

**Cozum:**

```SQL
SELECT rental_id, first_name, last_name FROM customer
FULL JOIN rental ON customer.customer_id = rental.customer_id;
```

**Sonuc:**

![Sonuc](/images/SqlOdev10_3.jpg)

