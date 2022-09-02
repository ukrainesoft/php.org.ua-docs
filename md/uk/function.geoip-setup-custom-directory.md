---
navigation:
  - function.geoip-region-name-by-code.md: « geoipregionnameбcode
  - function.geoip-time-zone-by-country-and-region.md: geoiptimezoneбcountryandregion »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoipsetupcustomdirectory
---
# geoipsetupcustomdirectory

(PECL geoip >= 1.1.0)

geoipsetupcustomdirectory — Встановити власну директорію для бази даних GeoIP

### Опис

```methodsynopsis
geoip_setup_custom_directory(string $path): void
```

Функція **geoipsetupcustomdirectory()** змінює каталог за промовчанням для бази даних GeoIP. Використання функції еквівалентно зміни [geoip.customdirectory](geoip.configuration.md#ini.geoip.custom-directory)

### Список параметрів

`path`

Повний шлях до бази даних GeoIP.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **geoipsetupcustomdirectory()****

Змінимо шлях до бази даних GeoIP.

```php
<?php

geoip_setup_custom_directory('/some/other/path');

print geoip_db_filename(GEOIP_COUNTRY_EDITION);

?>
```

Результат виконання цього прикладу:

```
/some/other/path/GeoIP.dat
```
