---
navigation:
  - function.filectime.md: « filectime
  - function.fileinode.md: fileinode »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: filegroup
---
# filegroup

(PHP 4, PHP 5, PHP 7, PHP 8)

filegroup — Отримує ідентифікатор групи файлу

### Опис

```methodsynopsis
filegroup(string $filename): int|false
```

Повертає ідентифікатор групи файлу як числа. Для отримання імені групи у вигляді рядка використовуйте функцію [posixgetgrgid()](function.posix-getgrgid.md)

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає ідентифікатор групи файлу або **`false`** у разі помилки. Ідентифікатор групи повертається у вигляді числа, для отримання імені групи у вигляді рядка використовуйте функцію [posixgetgrgid()](function.posix-getgrgid.md). У разі виникнення помилки повертається **`false`**

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

> **Зауваження**: Результати цієї функції кешуються Більш детальну інформацію дивіться у розділі [clearstatcache()](function.clearstatcache.md)

**Підказка**

Починаючи з PHP 5.0.0, ця функція також може бути використана з *деякими* обгортками url. Список обгорток, що підтримуються сімейством функцій [stat()](function.stat.md), дивіться у розділі [Підтримувані протоколи та обгортки](wrappers.md)

### Дивіться також

-   [fileowner()](function.fileowner.md) - Повертає ідентифікатор власника файлу
-   [posixgetgrgid()](function.posix-getgrgid.md) - Повертає інформацію про групу за її ID
