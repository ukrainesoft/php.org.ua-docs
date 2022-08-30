Повертає поточний процес SID

-   [« posixgetrlimit](function.posix-getrlimit.html)
    
-   [posixgetuid »](function.posix-getuid.html)
    
-   [PHP Manual](index.md)
    
-   [POSIX Функции](ref.posix.md)
    
-   Повертає поточний процес SID
    

# posixgetsid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetsid — Повертає поточний процес SID

### Опис

```methodsynopsis
posix_getsid(int $process_id): int|false
```

Повертає ідентифікатор сесії процесу `process_id`. Сесійний ідентифікатор процесу є ідентифікатор процесу лідера сеансу.

### Список параметрів

`process_id`

Ідентифікатор процесу. Якщо встановлено 0, мається на увазі поточний процес. Якщо передано некоректний `process_id`, то буде повернуто **`false`**. Також буде встановлено номер помилки, який можна обробити за допомогою функції [posixgetlasterror()](function.posix-get-last-error.html)

### Значення, що повертаються

Повертає ідентифікатор як int або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixgetsid()****

```php
<?php
$pid = posix_getpid();
echo posix_getsid($pid); //8805
?>
```

### Дивіться також

-   [posixgetpgid()](function.posix-getpgid.html) - Повертає ID групи поточного процесу для менеджера завдань
-   [posixsetsid()](function.posix-setsid.html) - Робить поточний процес лідером сесії
-   POSIX керівництво GETSID(2)