Перевіряє доступність бази GeoIP

-   [« geoipdatabaseinfo](function.geoip-database-info.html)
    
-   [geoipдбfilename »](function.geoip-db-filename.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Перевіряє доступність бази GeoIP
    

# geoipдбavail

(PECL geoip >= 1.0.1)

geoipдбavail — Перевірка доступності бази GeoIP

### Опис

```methodsynopsis
geoip_db_avail(int $database): bool
```

Функція **geoipдбavail()** визначає, чи доступна відповідна база GeoIP та чи може бути відкрита на диску.

При цьому не повідомляється, чи файл є коректною базою даних, тільки доступність для читання.

### Список параметрів

`database`

Тип бази даних визначається цілим числом (integer). Ви можете використовувати [различные константы](geoip.constants.html), визначені у цьому модулі (ie: GEOIPEDITION).

### Значення, що повертаються

Повертає **`true`**, якщо база даних існує, **`false`**, якщо не знайдена, або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **geoipдбavail()****

Приклад виводить версію поточної бази даних у вигляді рядка.

```php
<?php

if (geoip_db_avail(GEOIP_COUNTRY_EDITION))
    print geoip_database_info(GEOIP_COUNTRY_EDITION);
?>
```

Результат виконання цього прикладу:

```
GEO-106FREE 20080801 Build 1 Copyright (c) 2006 MaxMind LLC All Rights Reserved
```