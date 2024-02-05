---
navigation:
  - function.geoip-db-get-all-info.md: « geoip\_db\_get\_all\_info
  - function.geoip-id-by-name.md: geoip\_id\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_domain\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_domain\_by\_name

(PECL geoip >= 1.1.0)

geoip\_domain\_by\_name — Отримати назву домену другого рівня

### Опис

```methodsynopsis
geoip_domain_by_name(string $hostname): string
```

Функция**geoip\_domain\_by\_name()** повертає домени другого рівня, пов'язані з ім'ям хоста або IP-адресою.

Зараз ця функція доступна лише користувачам, які купили комерційну версію GeoIP Domain Edition. Якщо коректна база даних не буде знайдена, буде виведено попередження.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

У разі успішного виконання повертає ім'я домену. Якщо адреса не знайдена в базі, то повертається **`false`**

### Приклади

**Приклад #1 Приклад використання** geoip\_domain\_by\_name()\*\*\*\*

Знайдемо домен, пов'язаний із IP 61.106.139.1.

```php
<?php
$domain = geoip_domain_by_name('61.106.139.1');

if ($domain) {
    echo 'Домен: '. $domain;
}

?>
```

Результат виконання наведеного прикладу:

```
Домен: von.co.kr
```
