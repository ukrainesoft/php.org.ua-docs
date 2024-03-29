---
navigation:
  - function.geoip-country-code3-by-name.md: « geoip\_country\_code3\_by\_name
  - function.geoip-database-info.md: geoip\_database\_info »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_country\_name\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_country\_name\_by\_name

(PECL geoip >= 0.2.0)

geoip\_country\_name\_by\_name — Отримати повну назву країни

### Опис

```methodsynopsis
geoip_country_name_by_name(string $hostname): string
```

Функция**geoip\_country\_name\_by\_name()** повертає повну назву країни, що відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає повну назву країни при знаходженні адреси в базі даних, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання** geoip\_country\_name\_by\_name()\*\*\*\*

Цей приклад виведе розташування хоста example.com.

```php
<?php
$country = geoip_country_name_by_name('www.example.com');
if ($country) {
    echo 'Хост расположен в ' . $country;
}
?>
```

Результат виконання наведеного прикладу:

```
Хост расположен в United States
```

### Дивіться також

-   [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.md) \- Отримати двосимвольний код країни
-   [geoip\_country\_code3\_by\_name()](function.geoip-country-code3-by-name.md) \- Отримати трисимвольний код країни
