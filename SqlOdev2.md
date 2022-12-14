# Patika.dev SQL dersi
## Odev 2

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

**1. film tablosunda bulunan tüm sütunlardaki verileri replacement cost değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla sıralayınız ( BETWEEN - AND yapısını kullanınız.)**

***Cozum:***

Bu sorunun cozumunu asagidaki gibi bir query ile alabiliriz:

```SQL
SELECT * FROM film 
WHERE replacement_cost BETWEEN 12.99 AND 16.99;
```

![Sonuc 1](https://github.com/ErincT/patika.dev_Projelerim/blob/48b8608790f6f9c7e2920841b412164f6a07908c/images/SqlOdev2_1.jpg)

**2. actor tablosunda bulunan first_name ve last_name sütunlardaki verileri first_name 'Penelope' veya 'Nick' veya 'Ed' değerleri olması koşuluyla sıralayınız. ( IN operatörünü kullanınız.)**

***Cozum:***

IN operatorunu kullanarak belirtilen parametrelerde bir query olusturalim:

```SQL
SELECT first_name, last_name FROM actor 
WHERE first_name in ('Penelope', 'Nick', 'Ed');
```

![Sonuc 2](https://github.com/ErincT/patika.dev_Projelerim/blob/84a04ecd82a1aa605e4e34e4d299cdb1d6def0e0/images/SqlOdev2_2.jpg)

**3. film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99, 2.99, 4.99 VE replacement_cost 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız. ( IN operatörünü kullanınız.)**

***Cozum:***

Ilgili filtrelemeleri yapmak icin IN operatorunu kullanarak bir query olusturalim:

```SQL
SELECT * FROM film 
WHERE rental_rate IN (0.99, 2.99, 4.99) AND replacement_cost IN (12.99, 15.99, 28.99);
```

![Sonuc 3](https://github.com/ErincT/patika.dev_Projelerim/blob/84a04ecd82a1aa605e4e34e4d299cdb1d6def0e0/images/SqlOdev2_3.jpg)
