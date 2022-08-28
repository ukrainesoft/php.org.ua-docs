Отримати двосимвольний код країни

-   [« geoip\_continent\_code\_by\_name](function.geoip-continent-code-by-name.html)
    
-   [geoip\_country\_code3\_by\_name »](function.geoip-country-code3-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Отримати двосимвольний код країни
    

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
$country = geoip_country_code_by_name('www.example.com');
if ($country) {
    echo 'Хост расположен в ' . $country;
}
?>
```

Результат виконання цього прикладу:

```
Хост расположен в US
```

### Примітки

**Застереження**

Будь ласка, ознайомтеся з повним списком допустимих значень, що повертаються, в тому числі і спеціальних кодів, тут [» http://www.maxmind.com/en/iso3166](http://www.maxmind.com/en/iso3166)

### Дивіться також

-   [geoip\_country\_code3\_by\_name()](function.geoip-country-code3-by-name.html) - Отримати трисимвольний код країни
-   [geoip\_country\_name\_by\_name()](function.geoip-country-name-by-name.html) - Отримати повну назву країни