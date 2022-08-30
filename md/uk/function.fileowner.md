Повертає ідентифікатор власника файлу

-   [« filemtime](function.filemtime.html)
    
-   [fileperms »](function.fileperms.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Повертає ідентифікатор власника файлу
    

# fileowner

(PHP 4, PHP 5, PHP 7, PHP 8)

fileowner — Повертає ідентифікатор власника файлу

### Опис

```methodsynopsis
fileowner(string $filename): int|false
```

Повертає ідентифікатор власника файлу

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає числовий ідентифікатор власника вказаного файлу або **`false`** у разі виникнення помилки. Щоб отримати ім'я власника як рядок, використовуйте функцію [posixgetpwuid()](function.posix-getpwuid.html)

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Знаходимо власника файлу**

```php
<?php
$filename = 'index.php';
print_r(posix_getpwuid(fileowner($filename)));
?>
```

### Примітки

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.html)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.html), дивіться у розділі [Підтримувані протоколи та обгортки](wrappers.html)

### Дивіться також

-   [filegroup()](function.filegroup.html) - Отримує ідентифікатор групи файлу
-   [stat()](function.stat.html) - Повертає інформацію про файл
-   [posixgetpwuid()](function.posix-getpwuid.html) - Повертає інформацію про користувача, використовуючи його ID