---
navigation:
  - function.inet-ntop.html: « inetntop
  - function.ip2long.html: ip2long »
  - index.html: PHP Manual
  - ref.network.html: Мережеві функції
title: inetpton
---
# inetpton

(PHP 5> = 5.1.0, PHP 7, PHP 8)

inetpton — Конвертує IP-адресу, що читається, в її упаковане подання inaddr

### Опис

```methodsynopsis
inet_pton(string $ip): string|false
```

Ця функція конвертує читану IPv4- або IPv6-адресу (якщо PHP був зібраний з підтримкою IPv6) на адресу, що відповідає 32-бітовій або 128-бітовій бінарній структурі.

### Список параметрів

`ip`

IPv4- або IPv6-адреса, що читається.

### Значення, що повертаються

Повертає виставу `in_addr` заданого у параметрі `ip` адреси, або **`false`** якщо заданий синтаксично невірний `ip` (наприклад, IPv4-адреса без точок або IPv6-адреса без двокрапок).

### Приклади

**Приклад #1 Приклад використання **inetpton()****

```php
<?php
$in_addr = inet_pton('127.0.0.1');

$in6_addr = inet_pton('::1');
?>
```

### Дивіться також

-   [ip2long()](function.ip2long.md) - Конвертує рядок, що містить IPv4-адресу в ціле число
-   [long2ip()](function.long2ip.md) - Конвертує ціле число в IPv4-адресу
-   [inetntop()](function.inet-ntop.md) - Конвертує упаковану інтернет-адресу в формат, що читається
