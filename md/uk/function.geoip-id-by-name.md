---
navigation:
  - function.geoip-domain-by-name.md: « geoip\_domain\_by\_name
  - function.geoip-isp-by-name.md: geoip\_isp\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_id\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_id\_by\_name

(PECL geoip >= 0.2.0)

geoip\_id\_by\_name — Повертає тип підключення до Інтернету.

### Опис

```methodsynopsis
geoip_id_by_name(string $hostname): int
```

Функция**geoip\_id\_by\_name()** повертає тип Інтернет-з'єднання відповідного імені хоста або IP-адреси.

Повертає числове значення, яке можна порівняти з константами:

-   GEOIP\_UNKNOWN\_SPEED
-   GEOIP\_DIALUP\_SPEED
-   GEOIP\_CABLEDSL\_SPEED
-   GEOIP\_CORPORATE\_SPEED

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, з'єднання з якими перевіряється.

### Значення, що повертаються

Повертає тип з'єднання.

### Приклади

**Пример #1 Пример использования**geoip\_id\_by\_name()\*\*\*\*

Виводить тип з'єднання для хоста example.com.

```php
<?php
$netspeed = geoip_id_by_name('www.example.com');

echo 'Тип Интернет-соединения: ';

switch ($netspeed) {
    case GEOIP_DIALUP_SPEED:
        echo 'dial-up';
        break;
    case GEOIP_CABLEDSL_SPEED:
        echo 'cable or DSL';
        break;
    case GEOIP_CORPORATE_SPEED:
        echo 'corporate';
        break;
    case GEOIP_UNKNOWN_SPEED:
    default:
        echo 'unknown';
}
?>
```

Результат виконання наведеного прикладу:

```
Тип Интернет-соединения: corporate
```
