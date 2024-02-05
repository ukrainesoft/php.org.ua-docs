---
navigation:
  - function.imap-open.md: « imap\_open
  - function.imap-qprint.md: imap\_qprint »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_ping
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_ping

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_ping — Перевіряє, чи активний потік IMAP.

### Опис

```methodsynopsis
imap_ping(IMAP\Connection $imap): bool
```

Функция**imap\_ping()** перевіряє, чи активний відкритий потік. Це допомагає дізнаватися, чи є нова пошта. Це пріоритетний спосіб перевірки появи нових повідомлень та аналог постійних з'єднань (keep alive) для серверів з налаштованим часом очікування неактивності.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо потік активний і **`false`**, якщо ні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Пример #1 Пример использования**imap\_ping()\*\*\*\*

```php
<?php

$imap = imap_open("{imap.example.org}", "mailadmin", "password");

// после некоторого ожидания
if (!imap_ping($imap)) {
    // производим переподключение
}

?>
```
