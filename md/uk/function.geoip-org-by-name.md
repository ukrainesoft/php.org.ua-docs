---
navigation:
  - function.geoip-netspeedcell-by-name.md: « geoip\_netspeedcell\_by\_name
  - function.geoip-record-by-name.md: geoip\_record\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_org\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_org\_by\_name

(PECL geoip >= 0.2.0)

geoip\_org\_by\_name — Повертає назву організації, яка володіє IP-адресою

### Опис

```methodsynopsis
geoip_org_by_name(string $hostname): string
```

Функция**geoip\_org\_by\_name()** повертає назву організації, яка володіє вказаною IP-адресою.

Ця функція доступна лише для тих, хто придбав комерційну версію GeoIP Organization, ISP або AS. Якщо такої бази немає, виводиться попередження.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

Повертає ім'я організації у разі успішного виконання або **`false`**, якщо адреса не може бути знайдена в базі даних.

### Приклади

**Приклад #1 Приклад використання**geoip\_org\_by\_name()\*\*\*\*

Буде виведено назву організації, якій належить IP-адреса хоста example.com.

```php
<?php
$org = geoip_org_by_name('www.example.com');
if ($org) {
    echo 'Владелец данного адреса: ' . $org;
}
?>
```

Результат виконання наведеного прикладу:

```
Владелец данного адреса: ICANN c/o Internet Assigned Numbers Authority
```
