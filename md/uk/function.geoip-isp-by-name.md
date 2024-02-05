---
navigation:
  - function.geoip-id-by-name.md: « geoip\_id\_by\_name
  - function.geoip-netspeedcell-by-name.md: geoip\_netspeedcell\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_isp\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_isp\_by\_name

(PECL geoip >= 1.0.2)

geoip\_isp\_by\_name — Повертає ім'я інтернет-провайдера (ISP)

### Опис

```methodsynopsis
geoip_isp_by_name(string $hostname): string
```

Функция**geoip\_isp\_by\_name()** повертає ім'я інтернет-провайдера (ISP) вказаної IP-адреси.

Ця функція доступна лише для тих, хто придбав комерційну версію GeoIP ISP. Якщо такої бази немає, виводиться попередження.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

Повертає ім'я ISP у разі успішного виконання або **`false`**, якщо адресу не знайдено у базі даних.

### Приклади

**Пример #1 Пример использования**geoip\_isp\_by\_name()\*\*\*\*

Відобразить ім'я ISP для хоста example.com.

```php
<?php
$isp = geoip_isp_by_name('www.example.com');
if ($isp) {
    echo 'Этот IP-адрес управляется провайдером: ' . $isp;
}
?>
```

Результат виконання наведеного прикладу:

```
Адрес управляется провайдером: ICANN c/o Internet Assigned Numbers Authority
```
