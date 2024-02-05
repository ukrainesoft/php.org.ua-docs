---
navigation:
  - function.posix-setuid.md: « posix\_setuid
  - function.posix-sysconf.md: posix\_sysconf »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_strerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_strerror

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

posix\_strerror — Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки

### Опис

```methodsynopsis
posix_strerror(int $error_code): string
```

Повертає POSIX системне повідомлення про помилку, пов'язане з отриманим параметром `error_code` номером. Ви можете отримати параметр `error_code` за допомогою виклику функції [posix\_get\_last\_error()](function.posix-get-last-error.md)

### Список параметрів

`error_code`

POSIX номер помилки, отриманий із функції [posix\_get\_last\_error()](function.posix-get-last-error.md). . Якщо передано значення 0, буде повернено повідомлення "Success".

### Значення, що повертаються

Повертає рядок із повідомленням про помилку.

### Приклади

**Приклад #1 Приклад використання** posix\_strerror()\*\*\*\*

Цей скрипт намагається завершити неіснуючий процес, внаслідок чого буде виведено відповідне повідомлення про помилку.

```php
<?php
posix_kill(50,SIGKILL);
echo posix_strerror(posix_get_last_error())."\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
No such process
```

### Дивіться також

-   [posix\_get\_last\_error()](function.posix-get-last-error.md) \- Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею
