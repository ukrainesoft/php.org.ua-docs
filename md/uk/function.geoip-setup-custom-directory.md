---
navigation:
  - function.geoip-region-name-by-code.md: « geoip\_region\_name\_by\_code
  - function.geoip-time-zone-by-country-and-region.md: geoip\_time\_zone\_by\_country\_and\_region »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_setup\_custom\_directory
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_setup\_custom\_directory

(PECL geoip >= 1.1.0)

geoip\_setup\_custom\_directory — Встановити власну директорію для бази даних GeoIP

### Опис

```methodsynopsis
geoip_setup_custom_directory(string $path): void
```

Функция**geoip\_setup\_custom\_directory()** змінює каталог за промовчанням для бази даних GeoIP. Використання функції еквівалентно зміни [geoip.custom\_directory](geoip.configuration.md#ini.geoip.custom-directory)

### Список параметрів

`path`

Повний шлях до бази даних GeoIP.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** geoip\_setup\_custom\_directory()\*\*\*\*

Змінимо шлях до бази даних GeoIP.

```php
<?php

geoip_setup_custom_directory('/some/other/path');

print geoip_db_filename(GEOIP_COUNTRY_EDITION);

?>
```

Результат виконання наведеного прикладу:

```
/some/other/path/GeoIP.dat
```
