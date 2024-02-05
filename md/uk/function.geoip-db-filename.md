---
navigation:
  - function.geoip-db-avail.md: « geoip\_db\_avail
  - function.geoip-db-get-all-info.md: geoip\_db\_get\_all\_info »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_db\_filename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_db\_filename

(PECL geoip >= 1.0.1)

geoip\_db\_filename — Повертає ім'я файлу відповідної бази GeoIP

### Опис

```methodsynopsis
geoip_db_filename(int $database): string
```

Функция**geoip\_db\_filename()** повертає назву файлу відповідної бази GeoIP.

Функція не визначає, чи існує файл на диску, лише вказує шлях, яким бібліотека шукає файл бази.

### Список параметрів

`database`

Тип бази визначається цілим числом (integer). Ви можете використовувати [різноманітні константи](geoip.constants.md), визначені в цьому модулі (тобто: GEOIP\_\*\_EDITION).

### Значення, що повертаються

Повертає ім'я файлу відповідної бази, або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** geoip\_db\_filename()\*\*\*\*

Приклад відображення імені файлу поточної бази у вигляді рядка.

```php
<?php

print geoip_db_filename(GEOIP_COUNTRY_EDITION);

?>
```

Результат виконання наведеного прикладу:

```
/usr/share/GeoIP/GeoIP.dat
```
