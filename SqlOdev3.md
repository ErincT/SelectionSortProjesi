# Patika.dev SQL Dersi
## Odev 3

### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

### 1. country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
 
 **Cozum:** Ulke isminin `A` ile baslayip `a` ile bitmesini saglamak icin aralarina `%` isareti koyarak tirnak icersine aliriz. 
 
 ```SQL
SELECT country FROM country 
WHERE country LIKE 'A%a';
 ```
Sonuc olarak istedigimiz veriyi asagidaki gibi elde ederiz:

![Sonuc 1](/images/SqlOdev3_1.jpg)


### 2. country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız. ###

**Cozum:** Burada en az 6 karakter olmasini saglamak icin 5 adet `_` ve 1 adet `%` isaretinin yanina `n` harfini koyuyoruz.

```SQL
SELECT country FROM country 
WHERE country LIKE '%_____n';
```

Sonucumuz asagidaki gibi listelenir:

![Sonuc 2](/images/SqlOdev3_2.jpg)

### 3. film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız. ###

**Cozum:** Bu query'de buyuk kucuk harf ayrimi yapmadan filtrelemek icin `ILIKE` ve yeterli miktarda `t` harfinin olmasini saglamak icin basina, sonuna ve aralarina `%` konulmus 4 adet `t` harfi ile filtreleme yapiyoruz:

```SQL
SELECT title FROM film 
WHERE title ILIKE '%t%t%t%t%';
```

Sonuc istedigimiz gibi asagidaki gibi listelenir:

![Sonuc 3](/images/SqlOdev3_3.jpg)

### 4. film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız. ###

**Cozum:** Son alistirmada ilgili filtrelerin arasina `AND` operatorunu koyarak query'mizi hazirlariz:

```SQL
SELECT * FROM film 
WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99;
```

Sonuc asagidaki gibi olur:

![Sonuc 4](/images/SqlOdev3_4.jpg)

