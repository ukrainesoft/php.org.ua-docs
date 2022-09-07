---
navigation:
  - ref.geoip.md: « Функции GeoIP
  - function.geoip-continent-code-by-name.md: geoipcontinentcodeбname »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoipAsnumбname
---
# geoipAsnumбname

(PECL geoip >= 1.1.0)

geoipAsnumбname — Отримати номер автономної системи (ASN)

### Опис

```methodsynopsis
geoip_asnum_by_name(string $hostname): string
```

Функція **geoipAsnumбname()** повертає номери автономної системи, пов'язані з IP-адресою.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

У разі успішного виконання, повертає ASN. Якщо адреса не знайдена в базі, то повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **geoipAsnumбname()****

Отримання ASN для хоста [www.example.com](http://www.example.com)

```php
<?php
$asn = geoip_asnum_by_name('www.example.com');

if ($asn) {
    echo 'ASN равен: '. $asn;
}
?>
```

Результат виконання цього прикладу:

```
ASN равен: AS15133 EdgeCast Networks, Inc
```
