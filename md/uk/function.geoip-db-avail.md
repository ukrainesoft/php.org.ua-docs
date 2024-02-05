---
navigation:
  - function.geoip-database-info.md: « geoip\_database\_info
  - function.geoip-db-filename.md: geoip\_db\_filename »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_db\_avail
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_db\_avail

(PECL geoip >= 1.0.1)

geoip\_db\_avail — Перевірка доступності бази GeoIP

### Опис

```methodsynopsis
geoip_db_avail(int $database): bool
```

Функция**geoip\_db\_avail()** визначає, чи доступна відповідна база GeoIP та чи може бути відкрита на диску.

При цьому не повідомляється, чи файл є коректною базою даних, тільки доступність для читання.

### Список параметрів

`database`

Тип бази даних визначається цілим числом (integer). Ви можете використовувати [різні константи](geoip.constants.md), визначені у цьому модулі (ie: GEOIP\_\*\_EDITION).

### Значення, що повертаються

Повертає **`true`**, якщо база даних існує, **`false`**, якщо не знайдена, або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** geoip\_db\_avail()\*\*\*\*

Приклад виводить версію поточної бази даних у вигляді рядка.

```php
<?php

if (geoip_db_avail(GEOIP_COUNTRY_EDITION))
    print geoip_database_info(GEOIP_COUNTRY_EDITION);
?>
```

Результат виконання наведеного прикладу:

```
GEO-106FREE 20080801 Build 1 Copyright (c) 2006 MaxMind LLC All Rights Reserved
```
