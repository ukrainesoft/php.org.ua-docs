---
navigation:
  - function.geoip-record-by-name.md: « geoip\_record\_by\_name
  - function.geoip-region-name-by-code.md: geoip\_region\_name\_by\_code »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_region\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_region\_by\_name

(PECL geoip >= 0.2.0)

geoip\_region\_by\_name — Повертає коди країни та регіону

### Опис

```methodsynopsis
geoip_region_by_name(string $hostname): array
```

Функція**geoip\_region\_by\_name()** повертає коди країни та регіону, які відповідають імені хоста або IP-адреси.

Ця функція доступна лише для тих, хто придбав комерційну версію GeoIP Region. Якщо такої бази немає, виводиться попередження.

Наступні імена ключів асоціативного масиву, що повертається:

-   "country\_code" -- Двохлітерний код країни (дивіться [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.md)) .
-   "region" -- Код регіону (наприклад, CA для Каліфорнії)

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, дані про країну та регіон, якого потрібно знайти.

### Значення, що повертаються

Повертає асоціативний масив у разі успішного виконання або **`false`**, якщо адреса не буде знайдена у базі даних.

### Приклади

**Пример #1 Пример использования**geoip\_region\_by\_name()\*\*\*\*

Виведе масив, що складається з коду країни та регіону для хоста example.com.

```php
<?php
$region = geoip_region_by_name('www.example.com');
if ($region) {
    print_r($region);
}
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [country_code] => US
    [region] => CA
)
```
