## 1-) test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
CREATE TABLE employee(
	id SERIAL PRIMARY KEY,
	name VARCHAR(50) NOT NULL,
	birthday DATE,
	email VARCHAR(100)
);
## 2-) Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
Eklendi.
## 3-) Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.

1- UPDATE employee 
SET name = 'Test1'
WHERE email LIKE '%.net';

2- UPDATE employee 
SET email = 'Test2.@hotmail.com'
WHERE email LIKE '%.com';

3- UPDATE employee 
SET birthday = '1999-10-29',
	name = 'Test3'
WHERE id%2 = 0;

4- UPDATE employee
SET email = 'Test4@hotmail.com'
WHERE email ILIKE 'test2.%';

5- UPDATE employee 
SET name = 'Test5',
	birthday = '2000-01-01',
	email = 'example@hotmail.com'
WHERE id % 2 = 1;

## 4-) Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

1- DELETE FROM employee WHERE id = 10;

2- DELETE FROM employee WHERE email LIKE '%hotmail%';

3- DELETE FROM employee WHERE name ILIKE '%r%';

4- DELETE FROM employee WHERE name ILIKE 'a%' AND id = 3;

5- DELETE FROM employee;