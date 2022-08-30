Повертає ID групи поточного процесу для менеджера завдань

-   [« posixgetlogin](function.posix-getlogin.html)
    
-   [posixgetpgrp »](function.posix-getpgrp.html)
    
-   [PHP Manual](index.md)
    
-   [POSIX Функции](ref.posix.md)
    
-   Повертає ID групи поточного процесу для менеджера завдань
    

# posixgetpgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetpgid — Повертає ID групи поточного процесу для менеджера завдань

### Опис

```methodsynopsis
posix_getpgid(int $process_id): int|false
```

Повертає ідентифікатор групи поточного процесу . `process_id` або **`false`** у разі виникнення помилки.

### Список параметрів

`process_id`

Ідентифікатор поточного процесу.

### Значення, що повертаються

Повертає ідентифікатор як число int.

### Приклади

**Приклад #1 Приклад використання **posixgetpgid()****

```php
<?php
$pid = posix_getppid();
echo posix_getpgid($pid); //35
?>
```

### Примітки

> **Зауваження**
> 
> Це не POSIX функція, але вона сумісна з BSD та System V операційними системами. Якщо операційна система не підтримує цю функцію, вона не буде увімкнена при компіляції. Доступність цієї функції може бути перевірена за допомогою [functionexists()](function.function-exists.html)

### Дивіться також

-   [posixgetppid()](function.posix-getppid.html) - Повертає ідентифікатор батьківського процесу
-   керівництво SETPGID(2)