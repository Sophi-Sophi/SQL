**Задание: 1**
Найдите номер модели, скорость и размер жесткого диска для всех ПК стоимостью менее 500 дол. Вывести: model, speed и hd
-------------
SELECT model, speed, hd  
FROM pc  
WHERE price<500  
****

**Задание: 2**
Найдите производителей принтеров. Вывести: maker
-------------
SELECT DISTINCT maker <br/>
FROM Product<br/>
WHERE type='Printer'<br/>
****

**Задание: 3**
Найдите номер модели, объем памяти и размеры экранов ПК-блокнотов, цена которых превышает 1000 дол.
-------------
SELECT model,ram,screen
FROM Laptop
WHERE price>1000
****

**Задание: 4**
Найдите все записи таблицы Printer для цветных принтеров.
-------------
SELECT *
FROM Printer
WHERE color='y'
****

**Задание: 5**
Найдите номер модели, скорость и размер жесткого диска ПК, имеющих 12x или 24x CD и цену менее 600 дол.
-------------
SELECT model, speed, hd
FROM pc
WHERE price<600 AND ( cd='12x' OR cd='24x' )
***

**Задание: 6**
Для каждого производителя, выпускающего ПК-блокноты c объёмом жесткого диска не менее 10 Гбайт, найти скорости таких ПК-блокнотов.
Вывод: производитель, скорость.
-------------
SELECT DISTINCT product.maker, laptop.speed
FROM  product JOIN laptop
ON product.model=laptop.model
WHERE laptop.hd>=10
ORDER BY product.maker
***

**Задание: 7**
Найдите номера моделей и цены всех имеющихся в продаже продуктов (любого типа) производителя B (латинская буква).
--------------
SELECT DISTINCT Product.model, PC.price
FROM  Product JOIN PC
ON Product.model=PC.model
WHERE maker='B'
UNION
SELECT DISTINCT Product.model, Laptop.price
FROM  Product JOIN Laptop
ON Product.model=Laptop.model
WHERE maker='B'
UNION
SELECT DISTINCT Product.model, Printer.price
FROM  Product JOIN Printer
ON Product.model=Printer.model
WHERE maker='B'
***






