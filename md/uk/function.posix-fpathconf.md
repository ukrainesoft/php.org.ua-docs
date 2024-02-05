---
navigation:
  - function.posix-errno.md: « posix\_errno
  - function.posix-get-last-error.md: posix\_get\_last\_error »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_fpathconf
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_fpathconf

(PHP 8 >= 8.3.0)

posix\_fpathconf — Повертає значення обмеження, що настроюється.

### Опис

```methodsynopsis
posix_fpathconf(resource|int $file_descriptor, int $name): int|false
```

Повертає значення настроюваного обмеження з імені `name` ресурсу файлового дескриптора `resource`

### Список параметрів

`file_descriptor`

Файловий дескриптор, який очікується у вигляді ресурсу або ресурсу або цілого числа int. Під int мається на увазі файловий дескриптор, який можна передати безпосередньо до базового системного виклику.

`name`

Як ім'я обмеження, що налаштовується, дозволено вказувати одну з наступних констант: **`POSIX_PC_LINK_MAX`** **`POSIX_PC_MAX_CANON`** **`POSIX_PC_MAX_INPUT`** **`POSIX_PC_NAME_MAX`** **`POSIX_PC_PATH_MAX`** **`POSIX_PC_PIPE_BUF`** **`POSIX_PC_CHOWN_RESTRICTED`** **`POSIX_PC_NO_TRUNC`** **`POSIX_PC_ALLOC_SIZE_MIN`** **`POSIX_PC_SYMLINK_MAX`**

### Значення, що повертаються

Повертає обмеження, що налаштовується, або **`false`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md), если значение параметра`resource`недопустимо.

### Приклади

**Пример #1 Пример использования функции**posix\_fpathconf()\*\*\*\*

У цьому прикладі буде отримано максимальну довжину імені шляху в байтах для поточної директори.

```php
<?php

$fd = fopen(__DIR__, "r");
echo posix_fpathconf($fd, POSIX_PC_PATH_MAX);
?>
```

Результат виконання наведеного прикладу:

```
4096
```

### Примітки

### Дивіться також

-   [posix\_pathconf()](function.posix-pathconf.md) \- Повертає значення настроюваного обмеження
