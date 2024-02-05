---
navigation:
  - function.posix-mknod.md: « posix\_mknod
  - function.posix-setegid.md: posix\_setegid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_pathconf
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_pathconf

(PHP 8 >= 8.3.0)

posix\_pathconf — Повертає значення настроюваного обмеження

### Опис

```methodsynopsis
posix_pathconf(string $path, int $name): int|false
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Повертає значення настроюваного обмеження з імені `name`файла`file`

### Список параметрів

`path`

Ім'я файлу, обмеження якого потрібно отримати.

`name`

Як ім'я обмеження, що налаштовується, дозволено вказувати одну з наступних констант: **`POSIX_PC_LINK_MAX`** **`POSIX_PC_MAX_CANON`** **`POSIX_PC_MAX_INPUT`** **`POSIX_PC_NAME_MAX`** **`POSIX_PC_PATH_MAX`** **`POSIX_PC_PIPE_BUF`** **`POSIX_PC_CHOWN_RESTRICTED`** **`POSIX_PC_NO_TRUNC`** **`POSIX_PC_ALLOC_SIZE_MIN`** **`POSIX_PC_SYMLINK_MAX`**

### Значення, що повертаються

Повертає обмеження, що налаштовується, або **`false`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md)якщо шлях `path` виявиться порожнім.

### Приклади

**Приклад #1 Приклад використання функції** posix\_pathconf()\*\*\*\*

У цьому прикладі буде отримано максимальну довжину імені шляху в байтах для тимчасової директорії.

```php
<?php

echo posix_pathconf(sys_get_temp_dir(), POSIX_PC_PATH_MAX);
?>
```

Результат виконання наведеного прикладу:

```
4096
```

### Примітки

### Дивіться також

-   [posix\_fpathconf()](function.posix-fpathconf.md) \- Повертає значення настроюваного обмеження
