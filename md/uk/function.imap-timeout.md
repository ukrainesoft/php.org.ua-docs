---
navigation:
  - function.imap-thread.md: « imap\_thread
  - function.imap-uid.md: imap\_uid »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_timeout
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_timeout

(PHP 4 >= 4.3.3, PHP 5, PHP 7, PHP 8)

imap\_timeout — Встановлює або отримує час очікування imap

### Опис

```methodsynopsis
imap_timeout(int $timeout_type, int $timeout = -1): int|bool
```

Встановлює або отримує час очікування imap.

### Список параметрів

`timeout_type`

Одна из констант:**`IMAP_OPENTIMEOUT`** **`IMAP_READTIMEOUT`** **`IMAP_WRITETIMEOUT`**или**`IMAP_CLOSETIMEOUT`**

`timeout`

Час очікування за секунди.

### Значення, що повертаються

Если задан параметр`timeout`, ця функція поверне **`true`**или**`false`** залежно від успішності виконання.

Якщо параметр `timeout` не заданий, або виставлений рівним -1, то буде повернуто ціле число, що дорівнює поточній величині часу очікування, що відповідає заданому типу `timeout_type`

### Приклади

**Пример #1 Пример использования**imap\_timeout()\*\*\*\*

```php
<?php

echo "Текущее время ожидания чтения " . imap_timeout(IMAP_READTIMEOUT) . "\n";

?>
```
