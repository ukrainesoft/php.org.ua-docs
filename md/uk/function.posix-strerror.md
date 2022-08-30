Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки

-   [« posixsetuid](function.posix-setuid.html)
    
-   [posixtimes »](function.posix-times.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки
    

# posixstrerror

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

posixstrerror — Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки

### Опис

```methodsynopsis
posix_strerror(int $error_code): string
```

Повертає POSIX системне повідомлення про помилку, пов'язане з отриманим параметром `error_code` номером. Ви можете отримати параметр `error_code` за допомогою виклику функції [posixgetlasterror()](function.posix-get-last-error.html)

### Список параметрів

`error_code`

POSIX номер помилки, отриманий із функції [posixgetlasterror()](function.posix-get-last-error.html). Якщо передано значення 0, буде повернено повідомлення "Success".

### Значення, що повертаються

Повертає рядок із повідомленням про помилку.

### Приклади

**Приклад #1 Приклад використання **posixstrerror()****

Цей скрипт намагається завершити неіснуючий процес, внаслідок чого буде виведено відповідне повідомлення про помилку.

```php
<?php
posix_kill(50,SIGKILL);
echo posix_strerror(posix_get_last_error())."\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
No such process
```

### Дивіться також

-   [posixgetlasterror()](function.posix-get-last-error.html) - Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею