---
navigation:
  - function.posix-getrlimit.md: « posix\_getrlimit
  - function.posix-getuid.md: posix\_getuid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_getsid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_getsid

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_getsid — Повертає поточний процес SID

### Опис

```methodsynopsis
posix_getsid(int $process_id): int|false
```

Повертає ідентифікатор сесії процесу `process_id`. Сесійний ідентифікатор процесу є ідентифікатор процесу лідера сеансу.

### Список параметрів

`process_id`

Ідентифікатор процесу. Якщо встановлено 0, мається на увазі поточний процес. Якщо передано некоректний `process_id`, то буде повернуто **`false`**. Також буде встановлено номер помилки, який можна обробити за допомогою функції [posix\_get\_last\_error()](function.posix-get-last-error.md)

### Значення, що повертаються

Повертає ідентифікатор як int або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**posix\_getsid()\*\*\*\*

```php
<?php
$pid = posix_getpid();
echo posix_getsid($pid); //8805
?>
```

### Дивіться також

-   [posix\_getpgid()](function.posix-getpgid.md) \- Повертає ID групи поточного процесу для менеджера завдань
-   [posix\_setsid()](function.posix-setsid.md) \- Робить поточний процес лідером сесії
-   POSIX керівництво GETSID(2)
