Отримати повну назву країни

-   [« geoip\_country\_code3\_by\_name](function.geoip-country-code3-by-name.html)
    
-   [geoip\_database\_info »](function.geoip-database-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Отримати повну назву країни
    

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
$country = geoip_country_name_by_name('www.example.com');
if ($country) {
    echo 'Хост расположен в ' . $country;
}
?>
```

Результат виконання цього прикладу:

```
Хост расположен в United States
```

### Дивіться також

-   [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.html) - Отримати двосимвольний код країни
-   [geoip\_country\_code3\_by\_name()](function.geoip-country-code3-by-name.html) - Отримати трисимвольний код країни