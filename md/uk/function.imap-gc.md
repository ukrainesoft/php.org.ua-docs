---
navigation:
  - function.imap-fetchtext.md: « imap\_fetchtext
  - function.imap-get-quota.md: imap\_get\_quota »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_gc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_gc

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

imap\_gc — Очищає кеш IMAP

### Опис

```methodsynopsis
imap_gc(IMAP\Connection $imap, int $flags): true
```

Видаляє з кешу записи заданого типу.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`flags`

Задає кеш для чищення. Може бути будь-якою комбінацією констант: **`IMAP_GC_ELT`** (елементи кешу повідомлень), **`IMAP_GC_ENV`** (обгортки та тіла), **`IMAP_GC_TEXTS`** (Тексти).

### Значення, що повертаються

Функція завжди повертає **`true`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md), если значение параметра`flags`недопустимо.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | Тепер викидається виняток[ValueError](class.valueerror.md) при неприпустимих значеннях параметра `flags`. . Раніше виникало попередження та функція повертала логічне значення **`false`** |

### Приклади

**Приклад #1 Приклад використання** imap\_gc()\*\*\*\*

```php
<?php

$mbox = imap_open("{imap.example.org:143}", "username", "password");

imap_gc($mbox, IMAP_GC_ELT);

?>
```
