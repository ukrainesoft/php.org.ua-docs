---
navigation:
  - function.posix-getpid.md: « posix\_getpid
  - function.posix-getpwnam.md: posix\_getpwnam »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getppid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getppid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getppid — Повертає ідентифікатор батьківського процесу

### Опис

```methodsynopsis
posix_getppid(): int
```

Повертає ідентифікатор батьківського процесу стосовно поточного процесу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор процесу як int.

### Приклади

**Пример #1 Пример использования**posix\_getppid()\*\*\*\*

```php
<?php
echo posix_getppid(); //8259
?>
```
