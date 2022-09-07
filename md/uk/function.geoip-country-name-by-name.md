---
navigation:
  - function.geoip-country-code3-by-name.md: « geoipcountrycode3бname
  - function.geoip-database-info.md: geoipdatabaseinfo »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoipcountrynameбname
---
# geoipcountrynameбname

(PECL geoip >= 0.2.0)

geoipcountrynameбname — Отримати повну назву країни

### Опис

```methodsynopsis
geoip_country_name_by_name(string $hostname): string
```

Функція **geoipcountrynameбname()** повертає повну назву країни, що відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає повну назву країни при знаходженні адреси в базі даних, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **geoipcountrynameбname()****

Цей приклад виведе розташування хоста example.com.

```php
<?php
$country = geoip_country_name_by_name('www.example.com');
if ($country) {
    echo 'Хост расположен в ' . $country;
}
?>
```

Результат виконання цього прикладу:

```
Хост расположен в United States
```

### Дивіться також

-   [geoipcountrycodeбname()](function.geoip-country-code-by-name.md) - Отримати двосимвольний код країни
-   [geoipcountrycode3бname()](function.geoip-country-code3-by-name.md) - Отримати трисимвольний код країни
