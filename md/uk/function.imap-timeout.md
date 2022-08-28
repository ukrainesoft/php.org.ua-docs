Встановити або отримати час очікування imap

-   [« imap\_thread](function.imap-thread.html)
    
-   [imap\_uid »](function.imap-uid.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Встановити або отримати час очікування imap
    

# imaptimeout

(PHP 4> = 4.3.3, PHP 5, PHP 7, PHP 8)

imaptimeout — Встановити або отримати час очікування imap

### Опис

```methodsynopsis
imap_timeout(int $timeout_type, int $timeout = -1): int|bool
```

Встановлює або отримує час очікування imap.

### Список параметрів

`timeout_type`

Одна з констант: **`IMAP_OPENTIMEOUT`** **`IMAP_READTIMEOUT`** **`IMAP_WRITETIMEOUT`** або **`IMAP_CLOSETIMEOUT`**

`timeout`

Час очікування за секунди.

### Значення, що повертаються

Якщо встановлено параметр `timeout`, ця функція поверне **`true`** або **`false`** залежно від успішності виконання.

Якщо параметр `timeout` не заданий, або виставлений рівним -1, то буде повернено ціле число, що дорівнює поточній величині часу очікування, що відповідає заданому типу `timeout_type`

### Приклади

**Приклад #1 Приклад використання **imaptimeout()****

```php
<?php

echo "Текущее время ожидания чтения " . imap_timeout(IMAP_READTIMEOUT) . "\n";

?>
```