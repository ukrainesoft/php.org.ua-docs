---
navigation:
  - function.posix-getrlimit.md: « posixgetrlimit
  - function.posix-getuid.md: posixgetuid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixgetsid
---
# posixgetsid

(PHP 4, PHP 5, PHP 7, PHP 8)

posixgetsid — Повертає поточний процес SID

### Опис

```methodsynopsis
posix_getsid(int $process_id): int|false
```

Повертає ідентифікатор сесії процесу `process_id`. Сесійний ідентифікатор процесу є ідентифікатор процесу лідера сеансу.

### Список параметрів

`process_id`

Ідентифікатор процесу. Якщо встановлено 0, мається на увазі поточний процес. Якщо передано некоректний `process_id`, то буде повернуто **`false`**. Також буде встановлено номер помилки, який можна обробити за допомогою функції [posixgetlasterror()](function.posix-get-last-error.md)

### Значення, що повертаються

Повертає ідентифікатор як int або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixgetsid()****

```php
<?php
$pid = posix_getpid();
echo posix_getsid($pid); //8805
?>
```

### Дивіться також

-   [posixgetpgid()](function.posix-getpgid.md) - Повертає ID групи поточного процесу для менеджера завдань
-   [posixsetsid()](function.posix-setsid.md) - Робить поточний процес лідером сесії
-   POSIX керівництво GETSID(2)
