Отримати трисимвольний код країни

-   [« geoipcountrycodeбname](function.geoip-country-code-by-name.html)
    
-   [geoipcountrynameбname »](function.geoip-country-name-by-name.html)
    
-   [PHP Manual](index.md)
    
-   [Функции GeoIP](ref.geoip.md)
    
-   Отримати трисимвольний код країни
    

# geoipcountrycode3бname

(PECL geoip >= 0.2.0)

geoipcountrycode3бname — Отримати трисимвольний код країни

### Опис

```methodsynopsis
geoip_country_code3_by_name(string $hostname): string
```

Функція **geoipcountrycode3бname()** повертає трисимвольний код країни, який відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає три символи, що містять код континенту ISO 3166-1, при знаходженні адреси в базі даних, в іншому випадку **`false`**

### Приклади

**Приклад #1 Приклад використання **geoipcountrycode3бname()****

Цей приклад виведе розташування хоста example.com.

```php
<?php
$country = geoip_country_code3_by_name('www.example.com');
if ($country) {
    echo 'Хост расположен в ' . $country;
}
?>
```

Результат виконання цього прикладу:

```
Хост расположен в USA
```

### Дивіться також

-   [geoipcountrycodeбname()](function.geoip-country-code-by-name.html) - Отримати двосимвольний код країни
-   [geoipcountrynameбname()](function.geoip-country-name-by-name.html) - Отримати повну назву країни