---
navigation:
  - function.posix-kill.md: « posix\_kill
  - function.posix-mknod.md: posix\_mknod »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_mkfifo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_mkfifo

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_mkfifo - Створює спеціальний fifo файл (іменований канал-pipe)

### Опис

```methodsynopsis
posix_mkfifo(string $filename, int $permissions): bool
```

**posix\_mkfifo()** створює спеціальний `FIFO` файл, який існує у файловій системі і виступає як двоспрямований зв'язок для процесів.

### Список параметрів

`filename`

Шлях до `FIFO`файлу.

`permissions`

Другий параметр `permissions` має бути представлений у восьмеричній нотації (наприклад 0644). Це рівень прав для новоствореного `FIFO` файлу, також залежить від налаштувань поточного [umask()](function.umask.md). . Права на створений файл будуть визначатися як результат (mode & umask).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
