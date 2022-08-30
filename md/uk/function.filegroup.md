Отримує ідентифікатор групи файлу

-   [« filectime](function.filectime.html)
    
-   [fileinode »](function.fileinode.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Отримує ідентифікатор групи файлу
    

# filegroup

(PHP 4, PHP 5, PHP 7, PHP 8)

filegroup — Отримує ідентифікатор групи файлу

### Опис

```methodsynopsis
filegroup(string $filename): int|false
```

Повертає ідентифікатор групи файлу як числа. Для отримання імені групи у вигляді рядка використовуйте функцію [posixgetgrgid()](function.posix-getgrgid.html)

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає ідентифікатор групи файлу або **`false`** у разі помилки. Ідентифікатор групи повертається у вигляді числа, для отримання імені групи у вигляді рядка використовуйте функцію [posixgetgrgid()](function.posix-getgrgid.html). У разі виникнення помилки повертається **`false`**

### Помилки

У разі виникнення помилки буде згенеровано помилку рівня **`E_WARNING`**

### Приклади

**Приклад #1 Пошук групи файлів**

```php
<?php
$filename = 'index.php';
print_r(posix_getgrgid(filegroup($filename)));
?>
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.html)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.html), дивіться у розділі [Підтримувані протоколи та обгортки](wrappers.html)

### Дивіться також

-   [fileowner()](function.fileowner.html) - Повертає ідентифікатор власника файлу
-   [posixgetgrgid()](function.posix-getgrgid.html) - Повертає інформацію про групу за її ID