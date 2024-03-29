---
navigation:
  - function.posix-getsid.md: « posix\_getsid
  - function.posix-initgroups.md: posix\_initgroups »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getuid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getuid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getuid — Повертає фактичний ідентифікатор користувача для поточного процесу UID

### Опис

```methodsynopsis
posix_getuid(): int
```

Повертає число, що відповідає дійсному ID користувача поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ID користувача як int

### Приклади

**Приклад #1 Приклад використання** posix\_getuid()\*\*\*\*

```php
<?php
echo posix_getuid(); //10000
?>
```

### Дивіться також

-   [posix\_getpwuid()](function.posix-getpwuid.md) \- Повертає інформацію про користувача, використовуючи його ID
-   POSIX керівництво GETUID(2)
