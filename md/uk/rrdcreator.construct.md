Створює новий екземпляр RRDCreator

-   [« RRDCreator::addDataSource](rrdcreator.adddatasource.html)
    
-   [RRDCreator::save »](rrdcreator.save.html)
    
-   [PHP Manual](index.html)
    
-   [RRDCreator](class.rrdcreator.html)
    
-   Створює новий екземпляр RRDCreator
    

# RRDCreator::construct

(PECL rrd >= 0.9.0)

RRDCreator::construct — Створює новий екземпляр [RRDCreator](class.rrdcreator.html)

### Опис

public **RRDCreator::construct**(string `$path`, string `$startTime` =?, int `$step`

Створює новий екземпляр [RRDCreator](class.rrdcreator.html)

### Список параметрів

`path`

Шлях до створеного файлу бази даних RRD.

`startTime`

Час для першого значення бази даних RRD. Параметр підтримує всі формати, які підтримуються викликом rrd create.

int`step`

Базовий інтервал у секундах, з яким дані завантажуватимуться в базу даних RRD.