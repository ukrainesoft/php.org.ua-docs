---
navigation:
  - function.geoip-org-by-name.md: « geoip\_org\_by\_name
  - function.geoip-region-by-name.md: geoip\_region\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_record\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_record\_by\_name

(PECL geoip >= 0.2.0)

geoip\_record\_by\_name — Повертає детальну інформацію про адресу, знайдену в базі GeoIP

### Опис

```methodsynopsis
geoip_record_by_name(string $hostname): array
```

Функция**geoip\_record\_by\_name()** повертає інформацію про адресу, що відповідає імені хоста або IP-адреси.

Функція доступна для безкоштовної версії GeoLite City Edition та комерційної GeoIP City Edition. Якщо необхідних баз немає, виводиться попередження.

Наступні імена ключів асоціативного масиву, що повертається:

-   "continent\_code" - Дволітерний код континенту (з версії 1.0.4 з libgeoip 1.4.3 або новішої)
-   "country\_code" -- Двохлітерний код країни (дивіться [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.md)) .
-   "country\_code3" -- Трилітерний код країни (дивіться [geoip\_country\_code3\_by\_name()](function.geoip-country-code3-by-name.md)) .
-   "country\_name" -- Назва країни (дивіться [geoip\_country\_name\_by\_name()](function.geoip-country-name-by-name.md)) .
-   "region" -- Код регіону (наприклад: CA для Каліфорнії)
-   "City" - Місто.
-   "postal\_code" -- Поштовий індекс, FSA або Zip-код
-   " Latitude " -- Широта, число з плаваючою точкою (float) без знака.
-   "longitude" - Довгота, число з плаваючою точкою (float) без знака.
-   "dma\_code" -- Код ринкової зони (Designated Market Area, DMA), тільки для США та Канади
-   "area\_code" -- Код телефонної мережі загального користування (PSTN), наприклад, 212

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, дані за якою мають бути отримані.

### Значення, що повертаються

Повертає асоціативний масив у разі успішного виконання або \*\*`false`\*\*Якщо адреса не може бути знайдена в базі.

### список змін

| Версия | Опис |
| --- | --- |
| PECL geoip 1.0.4 | Додано код континенту (continent\_code) з GeoIP Library 1.4.3 або новішими. |
| PECL geoip 1.0.3 | Додано трилітерний код країни (country\_code3) та назва країни (country\_name). |

### Приклади

**Пример #1 Пример использования**geoip\_record\_by\_name()\*\*\*\*

Виведе масив, що містить запис про хост example.com.

```php
<?php
$record = geoip_record_by_name('www.example.com');
if ($record) {
    print_r($record);
}
?>
```

Результат виконання наведеного прикладу:

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
