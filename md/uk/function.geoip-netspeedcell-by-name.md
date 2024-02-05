---
navigation:
  - function.geoip-isp-by-name.md: « geoip\_isp\_by\_name
  - function.geoip-org-by-name.md: geoip\_org\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_netspeedcell\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_netspeedcell\_by\_name

(PECL geoip >= 1.1.0)

geoip\_netspeedcell\_by\_name — Отримати швидкість підключення до мережі Інтернет

### Опис

```methodsynopsis
geoip_netspeedcell_by_name(string $hostname): string
```

Функция**geoip\_netspeedcell\_by\_name()** повертає тип підключення до мережі Інтернет та його швидкість щодо заданого імені хоста або IP-адреси.

Ця функція доступна, лише якщо використовується бібліотека GeoIP версії 1.4.8 та вище.

Зараз ця функція доступна лише користувачам, які купили комерційну версію GeoIP Domain Edition. Якщо коректна база даних не буде знайдена, буде виведено попередження.

Повертається рядок. Стандартні значення:

-   Cable/DSL
-   Dialup
-   Cellular
-   Corporate

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

У разі успішного виконання повертає швидкість з'єднання. Якщо адреса не знайдена у базі даних, то повертається **`false`**

### Приклади

**Приклад #1 Приклад використання** geoip\_netspeedcell\_by\_name()\*\*\*\*

Отримання швидкості підключення до example.com.

```php
<?php
$netspeed = geoip_netspeedcell_by_name('www.example.com');

if ($netspeed) {
    echo 'Тип соединения: '. $netspeed;
}
?>
```

Результат виконання наведеного прикладу:

```
Тип соединения: Corporate
```
