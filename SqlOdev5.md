# Patika.dev SQL Dersi
## Odev 5

### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

### 1. film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.

**Cozum:** veri tablosu cok buyuk oldugu icin title ve length olarak gosterimini sinirliyoruz. 

```SQL
SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
```

Sonuc:

![Sonuc 1](/images/SqlOdev5_1.jpg)

### 2. film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.

**Cozum:**

```SQL
SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
OFFSET 5
LIMIT 5;
```

Sonuc:

![Sonuc 2](/images/SqlOdev5_2.jpg)


### 3. customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.

**Cozum:**

```SQL
SELECT * FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;
```

Sonuc:

![Sonuc 3](/images/SqlOdev5_3.jpg)
