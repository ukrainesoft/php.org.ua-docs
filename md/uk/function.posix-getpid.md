---
navigation:
  - function.posix-getpgrp.md: « posix\_getpgrp
  - function.posix-getppid.md: posix\_getppid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getpid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getpid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getpid — Повертає ідентифікатор поточного процесу

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

**Пример #1 Пример использования**posix\_getpid()\*\*\*\*

```php
<?php
echo posix_getpid(); //8805
?>
```

### Дивіться також

-   [posix\_kill()](function.posix-kill.md) \- Надсилає сигнал відповідному процесу
-   POSIX керівництво GETPID(2)
