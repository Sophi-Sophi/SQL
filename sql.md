**Задание: 1**
Найдите номер модели, скорость и размер жесткого диска для всех ПК стоимостью менее 500 дол. Вывести: model, speed и hd
-------------
SELECT model, speed, hd <br/>
FROM pc <br/>
WHERE price<500 <br/>
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
SELECT model,ram,screen <br/>
FROM Laptop <br/>
WHERE price>1000 <br/>
****

**Задание: 4**
Найдите все записи таблицы Printer для цветных принтеров.
-------------
SELECT * <br/>
FROM Printer <br/>
WHERE color='y' <br/>
****

**Задание: 5**
Найдите номер модели, скорость и размер жесткого диска ПК, имеющих 12x или 24x CD и цену менее 600 дол.
-------------
SELECT model, speed, hd <br/>
FROM pc <br/>
WHERE price<600 AND ( cd='12x' OR cd='24x' ) <br/>
***

**Задание: 6**
Для каждого производителя, выпускающего ПК-блокноты c объёмом жесткого диска не менее 10 Гбайт, найти скорости таких ПК-блокнотов.<br/>
Вывод: производитель, скорость.
-------------
SELECT DISTINCT product.maker, laptop.speed <br/>
FROM  product JOIN laptop <br/>
ON product.model=laptop.model <br/>
WHERE laptop.hd>=10 <br/>
ORDER BY product.maker <br/>
***

**Задание: 7**
Найдите номера моделей и цены всех имеющихся в продаже продуктов (любого типа) производителя B (латинская буква).
--------------
SELECT DISTINCT Product.model, PC.price <br/>
FROM  Product JOIN PC <br/>
ON Product.model=PC.model <br/>
WHERE maker='B' <br/>
UNION <br/>
SELECT DISTINCT Product.model, Laptop.price <br/>
FROM  Product JOIN Laptop <br/>
ON Product.model=Laptop.model <br/>
WHERE maker='B' <br/>
UNION <br/>
SELECT DISTINCT Product.model, Printer.price <br/>
FROM  Product JOIN Printer <br/>
ON Product.model=Printer.model <br/>
WHERE maker='B' <br/>
***






