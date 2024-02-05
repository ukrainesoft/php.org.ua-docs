---
navigation:
  - function.geoip-country-code-by-name.md: « geoip\_country\_code\_by\_name
  - function.geoip-country-name-by-name.md: geoip\_country\_name\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_country\_code3\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_country\_code3\_by\_name

(PECL geoip >= 0.2.0)

geoip\_country\_code3\_by\_name — Отримати трисимвольний код країни

### Опис

```methodsynopsis
geoip_country_code3_by_name(string $hostname): string
```

Функция**geoip\_country\_code3\_by\_name()** повертає трисимвольний код країни, який відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає три символи, що містять код континенту ISO 3166-1, при знаходженні адреси в базі даних, в іншому випадку **`false`**

### Приклади

**Приклад #1 Приклад використання** geoip\_country\_code3\_by\_name()\*\*\*\*

Цей приклад виведе розташування хоста example.com.

```php
<?php
$country = geoip_country_code3_by_name('www.example.com');
if ($country) {
    echo 'Хост расположен в ' . $country;
}
?>
```

Результат виконання наведеного прикладу:

```
Хост расположен в USA
```

### Дивіться також

-   [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.md) \- Отримати двосимвольний код країни
-   [geoip\_country\_name\_by\_name()](function.geoip-country-name-by-name.md) \- Отримати повну назву країни
