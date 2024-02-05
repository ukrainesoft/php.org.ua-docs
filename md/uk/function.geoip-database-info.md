---
navigation:
  - function.geoip-country-name-by-name.md: « geoip\_country\_name\_by\_name
  - function.geoip-db-avail.md: geoip\_db\_avail »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_database\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_database\_info

(PECL geoip >= 0.2.0)

geoip\_database\_info — Повертає інформацію про базу GeoIP

### Опис

```methodsynopsis
geoip_database_info(int $database = GEOIP_COUNTRY_EDITION): string
```

Функция**geoip\_database\_info()** повертає версію бази GeoIP, що відповідає визначенню у бінарному файлі.

Ця функція викликається без параметрів та повертає версію бази GeoIP Free Country Edition.

### Список параметрів

`database`

Тип бази визначається цілим числом (integer). Ви можете використовувати [різноманітні константи](geoip.constants.md), визначені в цьому модулі (тобто: GEOIP\_\*\_EDITION).

### Значення, що повертаються

Повертає відповідну версію, або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** geoip\_database\_info()\*\*\*\*

Приклад демонструє виведення інформації про базу даних.

```php
<?php
print geoip_database_info(GEOIP_COUNTRY_EDITION);
?>
```

Результат виконання наведеного прикладу:

```
GEO-106FREE 20060801 Build 1 Copyright (c) 2006 MaxMind LLC All Rights Reserved
```
