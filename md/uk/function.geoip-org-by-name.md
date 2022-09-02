---
navigation:
  - function.geoip-netspeedcell-by-name.md: « geoipnetspeedcellбname
  - function.geoip-record-by-name.md: geoiprecordбname »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoiporgбname
---
# geoiporgбname

(PECL geoip >= 0.2.0)

geoiporgбname — Повертає назву організації, яка володіє IP-адресою

### Опис

```methodsynopsis
geoip_org_by_name(string $hostname): string
```

Функція **geoiporgбname()** повертає назву організації, яка володіє вказаною IP-адресою.

Ця функція доступна лише для тих, хто придбав комерційну версію GeoIP Organization, ISP або AS. Якщо такої бази немає, виводиться попередження.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

Повертає ім'я організації у разі успішного виконання або **`false`**, якщо адреса не може бути знайдена в базі даних.

### Приклади

**Приклад #1 Приклад використання**geoiporgбname()\*\*\*\*

Буде виведено назву організації, якій належить IP-адреса хоста example.com.

```php
<?php
$org = geoip_org_by_name('www.example.com');
if ($org) {
    echo 'Владелец данного адреса: ' . $org;
}
?>
```

Результат виконання цього прикладу:

```
Владелец данного адреса: ICANN c/o Internet Assigned Numbers Authority
```
