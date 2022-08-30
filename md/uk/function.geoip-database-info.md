Повертає інформацію про базу GeoIP

-   [« geoipcountrynameбname](function.geoip-country-name-by-name.html)
    
-   [geoipдбavail »](function.geoip-db-avail.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Повертає інформацію про базу GeoIP
    

# geoipdatabaseinfo

(PECL geoip >= 0.2.0)

geoipdatabaseinfo — Повертає інформацію про базу GeoIP

### Опис

```methodsynopsis
geoip_database_info(int $database = GEOIP_COUNTRY_EDITION): string
```

Функція **geoipdatabaseinfo()** повертає версію бази GeoIP, що відповідає визначенню у бінарному файлі.

Ця функція викликається без параметрів та повертає версію бази GeoIP Free Country Edition.

### Список параметрів

`database`

Тип бази визначається цілим числом (integer). Ви можете використовувати [разнообразные константы](geoip.constants.html), визначені в цьому модулі (тобто: GEOIPEDITION).

### Значення, що повертаються

Повертає відповідну версію, або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **geoipdatabaseinfo()****

Приклад демонструє виведення інформації про базу даних.

```php
<?php
print geoip_database_info(GEOIP_COUNTRY_EDITION);
?>
```

Результат виконання цього прикладу:

```
GEO-106FREE 20060801 Build 1 Copyright (c) 2006 MaxMind LLC All Rights Reserved
```