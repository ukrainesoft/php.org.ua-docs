Створює новий екземпляр RRDCreator

-   [« RRDCreator::addDataSource](rrdcreator.adddatasource.md)
    
-   [RRDCreator::save »](rrdcreator.save.md)
    
-   [PHP Manual](index.md)
    
-   [RRDCreator](class.rrdcreator.md)
    
-   Створює новий екземпляр RRDCreator
    

# RRDCreator::construct

(PECL rrd >= 0.9.0)

RRDCreator::construct — Створює новий екземпляр [RRDCreator](class.rrdcreator.md)

### Опис

public **RRDCreator::construct**(string `$path`, string `$startTime` =?, int `$step`

Створює новий екземпляр [RRDCreator](class.rrdcreator.md)

### Список параметрів

`path`

Шлях до створеного файлу бази даних RRD.

`startTime`

Час для першого значення бази даних RRD. Параметр підтримує всі формати, які підтримуються викликом rrd create.

int`step`

Базовий інтервал у секундах, з яким дані завантажуватимуться в базу даних RRD.