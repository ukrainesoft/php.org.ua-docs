---
navigation:
  - function.geoip-continent-code-by-name.md: « geoipcontinentcodeбname
  - function.geoip-country-code3-by-name.md: geoipcountrycode3бname »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoipcountrycodeбname
---
# geoipcountrycodeбname

(PECL geoip >= 0.2.0)

geoipcountrycodeбname — Отримати двосимвольний код країни

### Опис

```methodsynopsis
geoip_country_code_by_name(string $hostname): string
```

Функція **geoipcountrycodeбname()** повертає двосимвольний код країни, який відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає два символи, що містять код країни за ISO 3166-1, при знаходженні адреси в базі даних, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **geoipcountrycodeбname()****

Цей приклад виведе розташування хоста example.com.

```php
<?php
$country = geoip_country_code_by_name('www.example.com');
if ($country) {
    echo 'Хост расположен в ' . $country;
}
?>
```

Результат виконання цього прикладу:

```
Хост расположен в US
```

### Примітки

**Застереження**

Будь ласка, ознайомтеся з повним списком допустимих значень, що повертаються, в тому числі і спеціальних кодів, тут [» http://www.maxmind.com/en/iso3166](http://www.maxmind.com/en/iso3166)

### Дивіться також

-   [geoipcountrycode3бname()](function.geoip-country-code3-by-name.md) - Отримати трисимвольний код країни
-   [geoipcountrynameбname()](function.geoip-country-name-by-name.md) - Отримати повну назву країни
