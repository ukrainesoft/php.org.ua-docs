Повертає коди країни та регіону

-   [« geoiprecordбname](function.geoip-record-by-name.html)
    
-   [geoipregionnameбcode »](function.geoip-region-name-by-code.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Повертає коди країни та регіону
    

# geoipregionбname

(PECL geoip >= 0.2.0)

geoipregionбname — Повертає коди країни та регіону

### Опис

```methodsynopsis
geoip_region_by_name(string $hostname): array
```

Функція**geoipregionбname()** повертає коди країни та регіону, які відповідають імені хоста або IP-адреси.

Ця функція доступна лише для тих, хто придбав комерційну версію GeoIP Region. Якщо такої бази немає, виводиться попередження.

Наступні імена ключів асоціативного масиву, що повертається:

-   " countrycode" -- Двохлітерний код країни (дивіться [geoipcountrycodeбname()](function.geoip-country-code-by-name.html)
-   "region" -- Код регіону (наприклад, CA для Каліфорнії)

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, дані про країну та регіон, якого потрібно знайти.

### Значення, що повертаються

Повертає асоціативний масив у разі успішного виконання або **`false`**, якщо адреса не буде знайдена у базі даних.

### Приклади

**Приклад #1 Приклад використання **geoipregionбname()****

Виведе масив, що складається з коду країни та регіону для хоста example.com.

```php
<?php
$region = geoip_region_by_name('www.example.com');
if ($region) {
    print_r($region);
}
?>
```

Результат виконання цього прикладу:

```
Array
(
    [country_code] => US
    [region] => CA
)
```