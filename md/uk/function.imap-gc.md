---
navigation:
  - function.imap-fetchtext.html: « imapfetchtext
  - function.imap-get-quota.html: imapgetquota »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
title: imapгк
---
# imapгк

(PHP 5> = 5.3.0, PHP 7, PHP 8)

imapgc — Очистити кеш IMAP

### Опис

```methodsynopsis
imap_gc(IMAP\Connection $imap, int $flags): bool
```

Видаляє з кешу записи заданого типу.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`flags`

Задає кеш для чищення. Може бути будь-якою комбінацією констант: **`IMAP_GC_ELT`** (елементи кешу повідомлень), **`IMAP_GC_ENV`** (обгортки та тіла), **`IMAP_GC_TEXTS`** (Тексти).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **imapgc()****

```php
<?php

$mbox = imap_open("{imap.example.org:143}", "username", "password");

imap_gc($mbox, IMAP_GC_ELT);

?>
```
