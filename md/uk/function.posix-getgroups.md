---
navigation:
  - function.posix-getgrnam.md: « posix\_getgrnam
  - function.posix-getlogin.md: posix\_getlogin »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getgroups
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getgroups

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getgroups — Повертає список груп для поточного процесу

### Опис

```methodsynopsis
posix_getgroups(): array|false
```

Повертає список груп для поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає числовий масив, що містить список ідентифікаторів груп для поточного процесу або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** posix\_getgroups()\*\*\*\*

```php
<?php

$groups = posix_getgroups();

print_r($groups);
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [posix\_getgrgid()](function.posix-getgrgid.md) \- Повертає інформацію про групу за її ID
