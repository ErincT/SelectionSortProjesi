# Patika.dev SQL Deris Odev 11

## 1. actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.

**Cozum**

```SQL
(
SELECT first_name FROM actor
)
UNION
(
SELECT first_name FROM customer
);
```

**Sonuc**

![Sonuc](/images/SqlOdev11_1.jpg)

## 2. actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.

**Cozum**

```SQL
(
SELECT first_name FROM actor
)
INTERSECT
(
SELECT first_name FROM customer
);
```

**Sonuc**

![Sonuc](/images/SqlOdev11_2.jpg)


## 3. actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.


**Cozum**

```SQL
(
SELECT first_name FROM actor
)
EXCEPT
(
SELECT first_name FROM customer
);
```

**Sonuc**

![Sonuc](/images/SqlOdev11_3.jpg)

## 4. İlk 3 sorguyu tekrar eden veriler için de yapalım.


**Cozum**

```SQL
(
SELECT first_name FROM actor
)
UNION ALL
(
SELECT first_name FROM customer
);
```

```SQL
(
SELECT first_name FROM actor
)
INTERSECT ALL
(
SELECT first_name FROM customer
);
```

```SQL
(
SELECT first_name FROM actor
)
EXCEPT ALL
(
SELECT first_name FROM customer
);
```
