---
navigation:
  - function.posix-getlogin.md: « posixgetlogin
  - function.posix-getpgrp.md: posixgetpgrp »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetpgid
---
# posixgetpgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetpgid — Повертає ID групи поточного процесу для менеджера завдань

### Опис

```methodsynopsis
posix_getpgid(int $process_id): int|false
```

Повертає ідентифікатор групи поточного процесу . `process_id` або **`false`** у разі виникнення помилки.

### Список параметрів

`process_id`

Ідентифікатор поточного процесу.

### Значення, що повертаються

Повертає ідентифікатор як число int.

### Приклади

**Приклад #1 Приклад використання **posixgetpgid()****

```php
<?php
$pid = posix_getppid();
echo posix_getpgid($pid); //35
?>
```

### Примітки

> **Зауваження**
> 
> Це не POSIX функція, але вона сумісна з BSD та System V операційними системами. Якщо операційна система не підтримує цю функцію, вона не буде увімкнена при компіляції. Доступність цієї функції може бути перевірена за допомогою [functionexists()](function.function-exists.md)

### Дивіться також

-   [posixgetppid()](function.posix-getppid.md) - Повертає ідентифікатор батьківського процесу
-   керівництво SETPGID(2)
