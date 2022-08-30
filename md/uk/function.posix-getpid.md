Повертає ідентифікатор поточного процесу

-   [« posixgetpgrp](function.posix-getpgrp.html)
    
-   [posixgetppid »](function.posix-getppid.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Повертає ідентифікатор поточного процесу
    

# posixgetpid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetpid — Повертає ідентифікатор поточного процесу

### Опис

```methodsynopsis
posix_getpid(): int
```

Повертає ідентифікатор поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор як int.

### Приклади

**Приклад #1 Приклад використання **posixgetpid()****

```php
<?php
echo posix_getpid(); //8805
?>
```

### Дивіться також

-   [posixkill()](function.posix-kill.html) - Надсилає сигнал відповідному процесу
-   POSIX керівництво GETPID(2)