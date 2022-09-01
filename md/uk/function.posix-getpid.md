---
navigation:
  - function.posix-getpgrp.html: « posixgetpgrp
  - function.posix-getppid.html: posixgetppid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetpid
---
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

-   [posixkill()](function.posix-kill.md) - Надсилає сигнал відповідному процесу
-   POSIX керівництво GETPID(2)
