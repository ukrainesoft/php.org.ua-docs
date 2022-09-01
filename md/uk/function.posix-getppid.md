---
navigation:
  - function.posix-getpid.html: « posixgetpid
  - function.posix-getpwnam.html: posixgetpwnam »
  - index.html: PHP Manual
  - ref.posix.html: POSIX Функции
title: posixgetppid
---
# posixgetppid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetppid — Повертає ідентифікатор батьківського процесу

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

**Приклад #1 Приклад використання **posixgetppid()****

```php
<?php
echo posix_getppid(); //8259
?>
```
