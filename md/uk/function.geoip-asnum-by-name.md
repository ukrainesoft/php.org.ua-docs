---
navigation:
  - ref.geoip.md: « Функції GeoIP
  - function.geoip-continent-code-by-name.md: geoip\_continent\_code\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_asnum\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_asnum\_by\_name

(PECL geoip >= 1.1.0)

geoip\_asnum\_by\_name — Отримати номер автономної системи (ASN)

### Опис

```methodsynopsis
geoip_asnum_by_name(string $hostname): string
```

Функция**geoip\_asnum\_by\_name()** повертає номери автономної системи, пов'язані з IP-адресою.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

У разі успішного виконання, повертає ASN. Якщо адреса не знайдена в базі, то повертається **`false`**

### Приклади

**Приклад #1 Приклад використання** geoip\_asnum\_by\_name()\*\*\*\*

Получение ASN для хоста[www.example.com](http://www.example.com)

```php
<?php
$asn = geoip_asnum_by_name('www.example.com');

if ($asn) {
    echo 'ASN равен: '. $asn;
}
?>
```

Результат виконання наведеного прикладу:

```
ASN равен: AS15133 EdgeCast Networks, Inc
```
