# Patika.dev SQL Dersi
## Odev 6


### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

### 1. film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

**Cozum:** Basit bir sorguyla cozumlere baslayalim

```SQL
SELECT AVG(rental_rate) FROM film;
```

Sonuc:

![Sonuc 1](/images/SqlOdev6_1.jpg)

### 2. film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

**Cozum:** `COUNT` ile satirlari saydirirken, `LIKE` ile `C` ile baslayan filmleri filtreliyoruz. 

```SQL
SELECT COUNT(*) from film
WHERE title LIKE 'C%';
```

Sonuc:

![Sonuc 2](/images/SqlOdev6_2.jpg)


### 3. film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

**Cozum:** Burada `MAX` kullanarak dogrudan sonuca ulasabiliriz. 

```SQL
SELECT MAX(length) FROM film
WHERE rental_rate = 0.99;
```

Sonuc:

![Sonuc 3](/images/SqlOdev6_3.jpg)


### 4. film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?


**Cozum:** `DISTINCT` kullanarak essiz `replacement_cost` degerlerini bulur, sonra `COUNT` ile saydirir ve `WHERE` ile filtreleriz. 

```SQL
SELECT COUNT(DISTINCT replacement_cost) FROM film
WHERE length > 150;
```

Sonuc:

![Sonuc 4](/images/SqlOdev6_4.jpg)
