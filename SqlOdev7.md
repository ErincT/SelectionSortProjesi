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

### 2. film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 

**Cozum**
```SQL
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost;
```

Sonuc

![Sonuc2](/images/SqlOdev7_2.jpg)

### 3. 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.

**Cozum**
```SQL
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY COUNT(*);
```

Sonuc

![Sonuc3](/images/SqlOdev7_3.jpg)
