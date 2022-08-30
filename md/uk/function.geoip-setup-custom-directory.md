Встановити власну директорію для бази даних GeoIP

-   [« geoipregionnameбcode](function.geoip-region-name-by-code.html)
    
-   [geoiptimezoneбcountryandregion »](function.geoip-time-zone-by-country-and-region.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Встановити власну директорію для бази даних GeoIP
    

# geoipsetupcustomdirectory

(PECL geoip >= 1.1.0)

geoipsetupcustomdirectory — Встановити власну директорію для бази даних GeoIP

### Опис

```methodsynopsis
geoip_setup_custom_directory(string $path): void
```

Функція **geoipsetupcustomdirectory()** змінює каталог за промовчанням для бази даних GeoIP. Використання функції еквівалентно зміни [geoip.customdirectory](geoip.configuration.html#ini.geoip.custom-directory)

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