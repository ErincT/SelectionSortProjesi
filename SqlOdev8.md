# Patika.dev SQL Dersi Odev 8

## 1. test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.

### Cozum:

```SQL
CREATE TABLE employee (
	id SERIAL PRIMARY KEY,
	name VARCHAR(50) NOT NULL,
	birthday DATE,
	email VARCHAR(100)
 );
```

Sonuc:

![Sonuc](/images/SqlOdev8_1.jpg)


## 2. Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

### Cozum:

```SQL
insert into employee (name, birthday, email) values ('Ursuline', '1998-11-03', 'upaolini0@wix.com');
insert into employee (name, birthday, email) values ('Maribeth', '1999-03-10', 'mneem1@businessinsider.com');
insert into employee (name, birthday, email) values ('Hunter', '1999-01-08', 'hrobers2@so-net.ne.jp');
insert into employee (name, birthday, email) values ('Cyril', '1980-10-08', 'chearfield3@google.pl');
insert into employee (name, birthday, email) values ('Corrie', '1973-12-20', 'cmarrison4@mac.com');
insert into employee (name, birthday, email) values ('Claribel', '2000-07-04', 'cciccoloi5@ovh.net');
insert into employee (name, birthday, email) values ('Easter', '1990-09-11', 'eblanc6@alexa.com');
insert into employee (name, birthday, email) values ('Roscoe', '1977-05-09', 'rsaul7@epa.gov');
insert into employee (name, birthday, email) values ('Peyter', '1971-12-15', 'pjurzyk8@dailymail.co.uk');
insert into employee (name, birthday, email) values ('Lotty', '1995-12-09', 'lplumbe9@berkeley.edu');
insert into employee (name, birthday, email) values ('Gearalt', '1992-11-26', 'gwanlessa@zimbio.com');
insert into employee (name, birthday, email) values ('Tannie', '1979-04-12', 'tdekeepb@ebay.com');
insert into employee (name, birthday, email) values ('Jenn', '1991-05-29', 'jyakunkinc@berkeley.edu');
insert into employee (name, birthday, email) values ('Audre', '1975-09-04', 'alaleveed@dropbox.com');
insert into employee (name, birthday, email) values ('Hugues', '1997-07-22', 'hstartee@statcounter.com');
insert into employee (name, birthday, email) values ('Guilbert', '1996-05-26', 'gordf@amazon.co.jp');
insert into employee (name, birthday, email) values ('Devan', '1975-12-28', 'dfitzharrisg@scientificamerican.com');
insert into employee (name, birthday, email) values ('Domenico', '2000-03-07', 'ddelvesh@vinaora.com');
insert into employee (name, birthday, email) values ('Ring', '1989-05-05', 'rvitleri@dailymail.co.uk');
insert into employee (name, birthday, email) values ('Krishnah', '1987-01-16', 'kcarranej@dailymotion.com');
insert into employee (name, birthday, email) values ('Perren', '1972-12-04', 'pfrankishk@earthlink.net');
insert into employee (name, birthday, email) values ('Cherri', '1999-05-30', 'ccowlandl@miibeian.gov.cn');
insert into employee (name, birthday, email) values ('Noe', '1989-01-08', 'nalloisim@house.gov');
insert into employee (name, birthday, email) values ('Marabel', '1990-04-03', 'mburkmann@dagondesign.com');
insert into employee (name, birthday, email) values ('Demetre', '1982-11-26', 'dsleanyo@stumbleupon.com');
insert into employee (name, birthday, email) values ('Bartolemo', '1973-07-15', 'bczajap@yandex.ru');
insert into employee (name, birthday, email) values ('Lucilia', '1972-01-30', 'lsinneyq@fastcompany.com');
insert into employee (name, birthday, email) values ('Salvatore', '1973-10-07', 'squereer@apple.com');
insert into employee (name, birthday, email) values ('Darin', '1975-07-07', 'dwharbys@smugmug.com');
insert into employee (name, birthday, email) values ('Julianna', '1998-04-18', 'jrosengartent@ed.gov');
insert into employee (name, birthday, email) values ('Fidelity', '1984-08-17', 'fchancelieru@google.co.jp');
insert into employee (name, birthday, email) values ('Sisely', '1973-11-23', 'stowllv@symantec.com');
insert into employee (name, birthday, email) values ('Hildagarde', '1996-08-17', 'hbyrdw@histats.com');
insert into employee (name, birthday, email) values ('Ashil', '1982-06-21', 'ahogbinx@taobao.com');
insert into employee (name, birthday, email) values ('Grata', '1987-03-23', 'gpotteridgey@ycombinator.com');
insert into employee (name, birthday, email) values ('Terrye', '1996-01-08', 'tridettz@freewebs.com');
insert into employee (name, birthday, email) values ('Wakefield', '1988-11-06', 'wmessingham10@g.co');
insert into employee (name, birthday, email) values ('Gustie', '1993-11-26', 'gswash11@google.cn');
insert into employee (name, birthday, email) values ('Garrott', '1989-01-15', 'gjodlkowski12@yahoo.co.jp');
insert into employee (name, birthday, email) values ('Bobbye', '1972-01-07', 'bbetteson13@surveymonkey.com');
insert into employee (name, birthday, email) values ('Clarinda', '1992-12-05', 'ceverit14@vistaprint.com');
insert into employee (name, birthday, email) values ('Odey', '1984-08-15', 'oaland15@weather.com');
insert into employee (name, birthday, email) values ('Ted', '1990-06-20', 'thasnney16@cam.ac.uk');
insert into employee (name, birthday, email) values ('Florance', '1993-03-27', 'fnewcomen17@com.com');
insert into employee (name, birthday, email) values ('Karleen', '1971-08-10', 'kschall18@delicious.com');
insert into employee (name, birthday, email) values ('Yves', '1987-10-26', 'yhaseley19@goodreads.com');
insert into employee (name, birthday, email) values ('Bibby', '1996-05-27', 'byakunikov1a@simplemachines.org');
insert into employee (name, birthday, email) values ('Rachelle', '1975-08-22', 'rkausche1b@deviantart.com');
insert into employee (name, birthday, email) values ('Christin', '1997-03-10', 'cpostles1c@mysql.com');
insert into employee (name, birthday, email) values ('Celle', '1989-06-07', 'csharnock1d@zdnet.com');

```

Sonuc:

![Sonuc](/images/SqlOdev8_2_1.jpg)
![Sonuc](/images/SqlOdev8_2_2.jpg)
![Sonuc](/images/SqlOdev8_2_3.jpg)


## 3. Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.


### Cozum:

Islem 1:

```SQL
UPDATE employee 
SET name = 'Emrah',
	email = 'emrah@emrah.com',
	birthday = '1979-01-01'
WHERE id =1
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_3_1.jpg)

Islem 2:

```SQL
UPDATE employee 
SET name = 'Ali',
	email = 'x@y.com',
	birthday = '2000-01-01'
WHERE name LIKE 'C%'
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_3_2.jpg)

Islem 3:

```SQL
UPDATE employee 
SET birthday = '2000-01-01'
WHERE birthday BETWEEN '1995-01-01' AND '2000-01-01'
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_3_3.jpg)


Islem 4:

```SQL
UPDATE employee 
SET email = ''
WHERE email LIKE 'a%'
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_3_4.jpg)

Islem 5:

```SQL
UPDATE employee 
SET email = '***'
WHERE name LIKE 'G%'
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_3_5.jpg)


## 4. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.


### Cozum:

Islem 1:

```SQL
DELETE FROM employee 
WHERE id = 3
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_4_1.jpg)

Islem 2:

```SQL
DELETE FROM employee 
WHERE id BETWEEN 5 AND 10
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_4_2.jpg)

Islem 3:

```SQL
DELETE FROM employee 
WHERE name LIKE 'A%'
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_4_3.jpg)

Islem 4:

```SQL
DELETE FROM employee 
WHERE birthday BETWEEN '1985-01-01' AND '1990-01-01'
RETURNING *;
```

Sonuc:

![Sonuc](/images/SqlOdev8_4_4.jpg)

Islem 5:

```SQL
DELETE FROM employee
WHERE name ILIKE '%a%t%'
RETURNING*;
```

Sonuc:

![Sonuc](/images/SqlOdev8_4_5.jpg)
