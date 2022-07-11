- [« RRDCreator::addDataSource](rrdcreator.adddatasource.md)
- [RRDCreator::save »](rrdcreator.save.md)

- [PHP Manual](index.md)
- [RRDCreator](class.rrdcreator.md)
- Створює новий екземпляр RRDCreator

# RRDCreator::\_\_construct

(PECL rrd \>= 0.9.0)

RRDCreator::\_\_construct — Створює новий екземпляр
[RRDCreator](class.rrdcreator.md)

### Опис

public **RRDCreator::\_\_construct**(string `$path`, string `$startTime`
= ?, int `$step` = 0)

Створює новий екземпляр [RRDCreator](class.rrdcreator.md).

### Список параметрів

`path`
Дорога до створеного файлу бази даних RRD.

`startTime`
Час для першого значення бази даних RRD. Параметр підтримує все
формати, що підтримуються викликом rrd create.

int`step`
Базовий інтервал у секундах, з яким дані завантажуватимуться в базу
даних RRD.
