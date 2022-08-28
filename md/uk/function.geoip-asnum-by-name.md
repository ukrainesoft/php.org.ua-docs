Отримати номер автономної системи (ASN)

-   [« Функции GeoIP](ref.geoip.html)
    
-   [geoip\_continent\_code\_by\_name »](function.geoip-continent-code-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Отримати номер автономної системи (ASN)
    

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
$asn = geoip_asnum_by_name('www.example.com');

if ($asn) {
    echo 'ASN равен: '. $asn;
}
?>
```

Результат виконання цього прикладу:

```
ASN равен: AS15133 EdgeCast Networks, Inc
```