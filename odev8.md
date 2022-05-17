## test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```
CREATE TABLE employee (
	id INTEGER,
	name VARCHAR(50),
	birthday DATE,
	emaiil VARCHAR(100)

);
```
## Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```
insert into employee (id, name, birthday, emaiil) values (1, 'Cassie', '1990-03-17', 'cgurys0@purevolume.com');
insert into employee (id, name, birthday, emaiil) values (2, 'Sissy', '1987-03-27', 'sleahey1@devhub.com');
insert into employee (id, name, birthday, emaiil) values (3, 'Walden', '1996-07-18', 'whardcastle2@pagesperso-orange.fr');
insert into employee (id, name, birthday, emaiil) values (4, 'Luciano', '1995-11-14', 'larmand3@nasa.gov');
insert into employee (id, name, birthday, emaiil) values (5, 'Dottie', '1982-11-14', 'dlaunchbury4@php.net');
insert into employee (id, name, birthday, emaiil) values (6, 'Hans', '1985-08-08', 'hwollard5@japanpost.jp');
.
.
.
```
## Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```
UPDATE employee
SET name = 'SQL'
WHERE id = 1
RETURNING *;

UPDATE employee
SET name = 'LSQ',
birthday = '1995-03-11'
WHERE id = 2
RETURNING *;

UPDATE employee
SET name = 'Maddy',
emaiil = 'voi@voi.com'
WHERE name = 'Cassie'
RETURNING *;

UPDATE employee
SET birthday = '1999-01-22'
WHERE id = '49';

UPDATE employee
SET name = '13'
WHERE birthday = '1999-01-22'
RETURNING *;

```
## Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```
DELETE FROM employee
WHERE birthday = '1999-01-22' ;

DELETE FROM employee
WHERE id = 1;

DELETE FROM employee
WHERE id > 47;

DELETE FROM employee
WHERE name = 'SQL';

DELETE FROM employee
WHERE birthday < '1999-01-22' 
RETURNING*;
```
