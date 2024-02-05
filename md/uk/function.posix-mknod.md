---
navigation:
  - function.posix-mkfifo.md: « posix\_mkfifo
  - function.posix-pathconf.md: posix\_pathconf »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_mknod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_mknod

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

posix\_mknod — Створює спеціальний або звичайний файл (POSIX.1)

### Опис

```methodsynopsis
posix_mknod(    string $filename,    int $flags,    int $major = 0,    int $minor = 0): bool
```

Створює спеціальний чи звичайний файл.

### Список параметрів

`filename`

Шлях та ім'я створюваного файлу

`flags`

Цей параметр виходить за допомогою побітового АБО між типом файлу (однієї з наступних констант: **`POSIX_S_IFREG`** **`POSIX_S_IFCHR`** **`POSIX_S_IFBLK`** **`POSIX_S_IFIFO`** або **`POSIX_S_IFSOCK`**) та правами доступу.

`major`

Старший номер пристрою (обов'язковий параметр під час використання констант **`S_IFCHR`** або **`S_IFBLK`**

`minor`

Молодший номер пристрою.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** posix\_mknod()\*\*\*\*

```php
<?php

$file = '/tmp/tmpfile';  // file name
$type = POSIX_S_IFBLK;   // file type
$permissions = 0777;     // octal
$major = 1;
$minor = 8;              // /dev/random

if (!posix_mknod($file, $type | $permissions, $major, $minor)) {
    die('Error ' . posix_get_last_error() . ': ' . posix_strerror(posix_get_last_error()));
}

?>
```

### Дивіться також

-   [posix\_mkfifo()](function.posix-mkfifo.md) \- Створює спеціальний fifo файл (іменований канал-pipe)
