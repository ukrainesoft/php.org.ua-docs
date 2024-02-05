---
navigation:
  - function.inet-ntop.md: « inet\_ntop
  - function.ip2long.md: ip2long »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: inet\_pton
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inet\_pton

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

inet\_pton — Конвертує IP-адресу, що читається, в її упаковане подання in\_addr

### Опис

```methodsynopsis
inet_pton(string $ip): string|false
```

Ця функція конвертує читану IPv4- або IPv6-адресу (якщо PHP був зібраний з підтримкою IPv6) на адресу, що відповідає 32-бітовій або 128-бітовій бінарній структурі.

### Список параметрів

`ip`

IPv4- або IPv6-адреса, що читається.

### Значення, що повертаються

Возвращает представление`in_addr`заданного в параметре`ip`адреса, или\*\*`false`\*\* якщо заданий синтаксично невірний `ip` (наприклад, IPv4-адреса без крапок або IPv6-адреса без двокрапок).

### Приклади

**Пример #1 Пример использования**inet\_pton()\*\*\*\*

```php
<?php
$in_addr = inet_pton('127.0.0.1');

$in6_addr = inet_pton('::1');
?>
```

### Дивіться також

-   [ip2long()](function.ip2long.md) \- Конвертує рядок, що містить IPv4-адресу в ціле число
-   [long2ip()](function.long2ip.md) \- Конвертує ціле число в IPv4-адресу
-   [inet\_ntop()](function.inet-ntop.md) \- Конвертує упаковану інтернет-адресу в формат, що читається
