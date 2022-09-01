---
navigation:
  - function.posix-getgrnam.html: « posixgetgrnam
  - function.posix-getlogin.html: posixgetlogin »
  - index.html: PHP Manual
  - ref.posix.html: POSIX Функции
title: posixgetgroups
---
# posixgetgroups

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetgroups — Повертає список груп для поточного процесу

### Опис

```methodsynopsis
posix_getgroups(): array|false
```

Повертає список груп для поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає числовий масив, що містить список ідентифікаторів груп для поточного процесу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixgetgroups()****

```php
<?php

$groups = posix_getgroups();

print_r($groups);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => 4
    [1] => 20
    [2] => 24
    [3] => 25
    [4] => 29
    [5] => 30
    [6] => 33
    [7] => 44
    [8] => 46
    [9] => 104
    [10] => 109
    [11] => 110
    [12] => 1000
)
```

### Дивіться також

-   [posixgetgrgid()](function.posix-getgrgid.md) - Повертає інформацію про групу за її ID
