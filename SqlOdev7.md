# Patika.dev SQL Dersi
## Odev 7

### 1. film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.

**Cozum** 

```SQL
SELECT rating FROM film
GROUP BY rating;
```

Sonuc

![Sonuc1](/images/SqlOdev7_1.jpg)

### 2. film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız

**Cozum**
```SQL
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY COUNT(*);
```

Sonuc

![Sonuc2](/images/SqlOdev7_3.jpg)

### 3. customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?

**Cozum**
```SQL
SELECT store_id, COUNT(customer_id) FROM customer
GROUP BY store_id;
```

Sonuc

![Sonuc3](/images/SqlOdev7_4.jpg)

###  4. city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.


**Cozum**
```SQL
SELECT country_id, COUNT(city) FROM city
GROUP BY country_id
ORDER BY count DESC
LIMIT 1;
```

Sonuc

![Sonuc3](/images/SqlOdev7_5.jpg)
