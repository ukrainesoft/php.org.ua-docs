Повертає тип інтернет-з'єднання

-   [« geoipdomainбname](function.geoip-domain-by-name.html)
    
-   [geoipispбname »](function.geoip-isp-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Повертає тип інтернет-з'єднання
    

# geoipідбname

(PECL geoip >= 0.2.0)

geoipідбname — Повертає тип підключення до Інтернету.

### Опис

```methodsynopsis
geoip_id_by_name(string $hostname): int
```

Функція **geoipідбname()** повертає тип Інтернет-з'єднання відповідного імені хоста або IP-адреси.

Повертає числове значення, яке можна порівняти з константами:

-   GEOIPUNKNOWNSPEED
-   GEOIPDIALUPSPEED
-   GEOIPCABLEDSLSPEED
-   GEOIPCORPORATESPEED

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, з'єднання з якими перевіряється.

### Значення, що повертаються

Повертає тип з'єднання.

### Приклади

**Приклад #1 Приклад використання **geoipідбname()****

Виводить тип з'єднання для хоста example.com.

```php
<?php
$netspeed = geoip_id_by_name('www.example.com');

echo 'Тип Интернет-соединения: ';

switch ($netspeed) {
    case GEOIP_DIALUP_SPEED:
        echo 'dial-up';
        break;
    case GEOIP_CABLEDSL_SPEED:
        echo 'cable or DSL';
        break;
    case GEOIP_CORPORATE_SPEED:
        echo 'corporate';
        break;
    case GEOIP_UNKNOWN_SPEED:
    default:
        echo 'unknown';
}
?>
```

Результат виконання цього прикладу:

```
Тип Интернет-соединения: corporate
```