---
navigation:
  - function.geoip-db-avail.html: « geoipдбavail
  - function.geoip-db-get-all-info.html: geoipдбgetallinfo »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoipдбfilename
---
# geoipдбfilename

(PECL geoip >= 1.0.1)

geoipдбfilename — Повертає ім'я файлу відповідної бази GeoIP

### Опис

```methodsynopsis
geoip_db_filename(int $database): string
```

Функція **geoipдбfilename()** повертає назву файлу відповідної бази GeoIP.

Функція не визначає, чи існує файл на диску, лише вказує шлях, яким бібліотека шукає файл бази.

### Список параметрів

`database`

Тип бази визначається цілим числом (integer). Ви можете використовувати [різноманітні константи](geoip.constants.md), визначені в цьому модулі (тобто: GEOIPEDITION).

### Значення, що повертаються

Повертає ім'я файлу відповідної бази, або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **geoipдбfilename()****

Приклад відображення імені файлу поточної бази у вигляді рядка.

```php
<?php

print geoip_db_filename(GEOIP_COUNTRY_EDITION);

?>
```

Результат виконання цього прикладу:

```
/usr/share/GeoIP/GeoIP.dat
```
