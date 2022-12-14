# Patika.dev SQL dersi 
## Odev 1

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

***1. film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.***

**Cozum:**
SELECT ifadesinden sonra istedigimiz kolon isimlerini virgul ile ayirarak yazar sonrasinda FROM ifadesi ile hangi veritabaninda calismak istedigimizi belirtiriz:

```SQL
SELECT title, description FROM film;
```
Bunun sonucunda asagidaki gibi bir sonuc olusturulur:

![1. sonuc](https://github.com/ErincT/patika.dev_Projelerim/blob/8d655dfb3f1da58956e718b946f503e32d0aa9b4/images/SqlOdev1_1.jpg)

***2. film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.***

**Cozum:**
Benzer sekilde SELECT ifadesini kullaniriz ancak bu sefer belirli kolonlari degil, butun kolonlari cagirmak istiyor oldugumuz icin yildiz '*' kullaniriz. 
Sonrasinda ise WHERE ifadesinin yanina filtrelemek istedigimiz kolon isimlerini gireriz. 
```SQL
SELECT * FROM film
WHERE length > 60 AND length < 75;
```
Sonuc olarak alacagimiz cikti: 

![2. sonuc](https://github.com/ErincT/patika.dev_Projelerim/blob/a1401fdc9aa759483a386817dc2f3d0c21623f24/images/SqlOdev1_2.jpg)

***3. film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.***

**Cozum**
Bu problemin cozumunde replacement_cost'lari parantez icerisine almamiz gerekiyor. Bunun nedeni ise OR ifadesini islem sirasinda ikinci sirada olmasi. 
```SQL
SELECT * FROM film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
```
Parantezleri kullandigimiz icin sonuc istedigimiz gibi oluyor: 

![3. sonuc](https://github.com/ErincT/patika.dev_Projelerim/blob/ded1d64f80cdc5c20eb5f9a0221f9f59232473a9/images/SqlOdev1_3.jpg)

***4. customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?***

**Cozum**
Bu yaniti almak icin bir ismi Mary olan customer'lari first_name, last_name olarak gosterecek bir query olusturalim:
```SQL
SELECT first_name, last_name FROM customer
WHERE first_name = 'Mary';
```
Sonuc olarak ilgili customer'in last_name hucresinde 'Smith' degerini bulduk: 

![4. sonuc](https://github.com/ErincT/patika.dev_Projelerim/blob/4a13ee9e67e9e17866ddf6ed4a04dbb41592c6b5/images/SqlOdev1_4.jpg)

***5. film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.***

**Cozum**
Sorunun icersiinde bulunan veya ifadesi aldatici bir sekilde bulunuyor olup, bu ifadeyi oldugu gibi kullandigimizda istedigimiz yaniti alamiyoruz. Bunun yerine asagidaki gibi asagidaki gibi AND ile filtrelememizi yapariz: 
```SQL
SELECT * FROM film
WHERE length < 50 AND rental_rate <> 2.99 AND rental_rate <> 4.99;
```
Sonuc olarak asagidaki gibi istedigimiz degerleri aliriz: 

![5. sonuc](https://github.com/ErincT/patika.dev_Projelerim/blob/7ab58a571265498630e3d2116edeec3bf8b31584/images/SqlOdev1_5.jpg)
