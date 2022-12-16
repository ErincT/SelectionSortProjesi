# Patika.dev SQL Dersi Odev 12


## 1. film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?

**Cozum:**

```SQL
SELECT COUNT(*) FROM film
WHERE length > ANY
(
SELECT AVG(length) FROM film
);
```

**Sonuc**

![Sonuc](/images/SqlOdev12_1.jpg)

## 2. film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?

**Cozum:**

```SQL
SELECT COUNT(*) FROM film
WHERE rental_rate = ANY
(
SELECT MAX(rental_rate) FROM film
);
```

**Sonuc**

![Sonuc](/images/SqlOdev12_2.jpg)

## 3. film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.

**Cozum:**

```SQL
SELECT title, rental_rate, replacement_cost FROM film
ORDER BY rental_rate, replacement_cost;
```

**Sonuc**

![Sonuc](/images/SqlOdev12_3.jpg)

## 4. payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

**Cozum:**

```SQL
SELECT DISTINCT customer.customer_id, first_name, last_name, COUNT(payment.customer_id) AS "ALISVERIS SAYISI" FROM payment
LEFT JOIN customer ON payment.customer_id = customer.customer_id
GROUP BY customer.customer_id
ORDER BY COUNT(payment.customer_id) DESC;
```

**Sonuc**

![Sonuc](/images/SqlOdev12_4.jpg)
