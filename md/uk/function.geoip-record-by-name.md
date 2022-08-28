Повертає докладну інформацію про адресу, знайдену в базі GeoIP

-   [« geoip\_org\_by\_name](function.geoip-org-by-name.html)
    
-   [geoip\_region\_by\_name »](function.geoip-region-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Повертає докладну інформацію про адресу, знайдену в базі GeoIP
    

# geoiprecordбname

(PECL geoip >= 0.2.0)

geoiprecordбname — Повертає детальну інформацію про адресу, знайдену в базі GeoIP

### Опис

```methodsynopsis
geoip_record_by_name(string $hostname): array
```

Функція **geoiprecordбname()** повертає інформацію про адресу, що відповідає імені хоста або IP-адреси.

Функція доступна для безкоштовної версії GeoLite City Edition та комерційної GeoIP City Edition. Якщо необхідних баз немає, виводиться попередження.

Наступні імена ключів асоціативного масиву, що повертається:

-   "continentcode" - Дволітерний код континенту (з версії 1.0.4 з libgeoip 1.4.3 або новішої)
-   " countrycode" -- Двохлітерний код країни (дивіться [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.html)
-   " countrycode3" -- Трилітерний код країни (дивіться [geoip\_country\_code3\_by\_name()](function.geoip-country-code3-by-name.html)
-   " countryname" -- Назва країни (дивіться [geoip\_country\_name\_by\_name()](function.geoip-country-name-by-name.html)
-   "region" -- Код регіону (наприклад: CA для Каліфорнії)
-   "City" - Місто.
-   "postalcode" -- Поштовий індекс, FSA або Zip-код
-   "latitude" - Широта, знакове речове число (signed double).
-   "longitude" - Довгота, знакове речове число (signed double).
-   "dmacode" -- Код ринкової зони (Designated Market Area, DMA), тільки для США та Канади
-   "areacode" -- Код телефонної мережі загального користування (PSTN), наприклад, 212

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, дані за якою мають бути отримані.

### Значення, що повертаються

Повертає асоціативний масив у разі успішного виконання або **`false`**Якщо адреса не може бути знайдена в базі.

### список змін

| Версия           | Описание                                                                    |
|------------------|-----------------------------------------------------------------------------|
| PECL geoip 1.0.4 | Додано код континенту (continentcode) з GeoIP Library 1.4.3 або новішими.   |
| PECL geoip 1.0.3 | Додано трилітерний код країни (countrycode3) та назва країни (countryname). |

### Приклади

**Приклад #1 Приклад використання **geoiprecordбname()****

Виведе масив, що містить запис про хост example.com.

```php
<?php
$record = geoip_record_by_name('www.example.com');
if ($record) {
    print_r($record);
}
?>
```

Результат виконання цього прикладу:

```
Array
(
    [continent_code] => NA
    [country_code] => US
    [country_code3] => USA
    [country_name] => United States
    [region] => CA
    [city] => Marina Del Rey
    [postal_code] =>
    [latitude] => 33.9776992798
    [longitude] => -118.435096741
    [dma_code] => 803
    [area_code] => 310
)
```