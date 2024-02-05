---
navigation:
  - function.http-response-code.md: « http\_response\_code
  - function.inet-pton.md: inet\_pton »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: inet\_ntop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inet\_ntop

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

inet\_ntop — Конвертує упаковану інтернет-адресу в формат, що читається

### Опис

```methodsynopsis
inet_ntop(string $ip): string|false
```

Ця функція конвертує 32-бітову IPv4 або 128-бітову IPv6-адресу (якщо PHP був зібраний з підтримкою IPv6) у відповідне рядкове подання адреси.

### Список параметрів

`ip`

32-бітова IPv4-адреса або 128-бітова IPv6-адреса.

### Значення, що повертаються

Возвращает строковое представление адреса или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** inet\_ntop()\*\*\*\*

```php
<?php
$packed = chr(127) . chr(0) . chr(0) . chr(1);
$expanded = inet_ntop($packed);

/* Выведет: 127.0.0.1 */
echo $expanded;

$packed = str_repeat(chr(0), 15) . chr(1);
$expanded = inet_ntop($packed);

/* Выведет: ::1 */
echo $expanded;
?>
```

### Дивіться також

-   [long2ip()](function.long2ip.md) \- Конвертує ціле число в IPv4-адресу
-   [ip2long()](function.ip2long.md) \- Конвертує рядок, що містить IPv4-адресу в ціле число
-   [inet\_pton()](function.inet-pton.md) \- Конвертує IP-адресу, що читається, в її упаковане подання in\_addr
