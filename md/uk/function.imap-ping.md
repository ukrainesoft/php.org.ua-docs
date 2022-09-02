---
navigation:
  - function.imap-open.md: « imapopen
  - function.imap-qprint.md: imapqprint »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapping
---
# imapping

(PHP 4, PHP 5, PHP 7, PHP 8)

imapping — Перевірити, чи активний потік IMAP

### Опис

```methodsynopsis
imap_ping(IMAP\Connection $imap): bool
```

**imapping()** перевіряє, чи активний відкритий потік. За допомогою нього можна дізнаватися, чи є нова пошта. Це кращий метод перевіряти чи є нові повідомлення та аналог "keep alive" для серверів з налаштованим часом очікування неактивності.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо потік активний і **`false`**, якщо ні.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapping()****

```php
<?php

$imap = imap_open("{imap.example.org}", "mailadmin", "password");

// после некоторого ожидания
if (!imap_ping($imap)) {
    // производим переподключение
}

?>
```
