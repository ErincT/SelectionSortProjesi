# Patika.dev SQL Dersi
## Odev 4

### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

### 1. film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.

**Cozum:** Asagidaki gibi ilgili kolondaki essiz verileri siralayabiliriz:

```SQL
SELECT DISTINCT replacement_cost FROM film;
```

Sonuc: 

![Sonuc 1](/images/SqlOdev4_1.jpg)

### 2. film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?

**Cozum:** 1. Cozumde uyguladigimiz query'ye sadece `COUNT` ekleyerek listemizi elde ederiz:

```SQL
SELECT COUNT(DISTINCT replacement_cost) FROM film;
```

Sonuc:

![Sonuc 2](/images/SqlOdev4_2.jpg)

### 3. film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?

**Cozum:** Onceki orneklerden biraz daha detayli olan bu ornekte, `COUNT` ve `DISTINCT` soz dizimlerini kullandiktan sonra `WHERE` ile filtremizi daraltiriz ve sonuca ulasiriz:

```SQL
SELECT COUNT(DISTINCT title) FROM film
WHERE title LIKE 'T%' AND rating = 'G';
```

Sonuc:

![Sonuc 3](/images/SqlOdev4_3.jpg)

### 4. country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?

**Cozum:** Bu alistirmada `LIKE` soz dizimini kullanarak query'mizi daraltabiliriz.

```SQL
SELECT COUNT(DISTINCT country) FROM country
WHERE country LIKE '_____';
```

Sonuc:

![Sonuc 4](/images/SqlOdev4_4.jpg)

### 5. city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?

**Cozum:** Son ornegimizde `ILIKE` kullanmamiz gerekecektir. Bu sekilde buyuk kucuk harf ayrimi olmaksizin aramamizi yapabiliyoruz. 

```SQL
SELECT COUNT(DISTINCT city) FROM city
WHERE city ILIKE '%r';
```

Sonuc:

![Sonuc 5](/images/SqlOdev4_5.jpg)
