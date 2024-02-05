---
navigation:
  - function.posix-getlogin.md: « posix\_getlogin
  - function.posix-getpgrp.md: posix\_getpgrp »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getpgid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getpgid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getpgid — Повертає ID групи поточного процесу для менеджера завдань

### Опис

```methodsynopsis
posix_getpgid(int $process_id): int|false
```

Повертає ідентифікатор групи поточного процесу . `process_id`или\*\*`false`\*\*в случае возникновения ошибки.

### Список параметрів

`process_id`

Ідентифікатор поточного процесу.

### Значення, що повертаються

Повертає ідентифікатор як число int.

### Приклади

**Приклад #1 Приклад використання** posix\_getpgid()\*\*\*\*

```php
<?php
$pid = posix_getppid();
echo posix_getpgid($pid); //35
?>
```

### Примітки

> **Зауваження** :
> 
> Це не POSIX функція, але вона сумісна з BSD та System V операційними системами. Якщо операційна система не підтримує цю функцію, вона не буде увімкнена при компіляції. Доступність цієї функції може бути перевірена за допомогою [function\_exists()](function.function-exists.md)

### Дивіться також

-   [posix\_getppid()](function.posix-getppid.md) \- Повертає ідентифікатор батьківського процесу
-   керівництво SETPGID(2)
