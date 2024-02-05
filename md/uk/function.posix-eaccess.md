---
navigation:
  - function.posix-ctermid.md: « posix\_ctermid
  - function.posix-errno.md: posix\_errno »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_eaccess
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_eaccess

(PHP 8 >= 8.3.0)

posix\_eaccess — Визначає доступність файлу

### Опис

```methodsynopsis
posix_eaccess(string $filename, int $flags = 0): bool
```

Функция**posix\_eaccess()** перевіряє права доступу чинного користувача до файлу.

### Список параметрів

`filename`

Ім'я файлу для перевірки.

`flags`

Маска, що складається з однієї або кількох констант: **`POSIX_F_OK`** **`POSIX_R_OK`** **`POSIX_W_OK`** і **`POSIX_X_OK`**

Константи **`POSIX_R_OK`** **`POSIX_W_OK`** і **`POSIX_X_OK`** запитують перевірку існування файлу та наявності дозволів на читання, запис та виконання відповідно. Константа **`POSIX_F_OK`** просто запитує перевірку існування файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Перевіряє права чинного користувача/групи на файл, на відміну функції [posix\_access()](function.posix-access.md)яка перевіряє реального користувача/групу. |

### Приклади

**Приклад #1 Приклад використання функції** posix\_eaccess()\*\*\*\*

У цьому прикладі буде перевірено, чи доступний файл у змінній $file для читання та запису, інакше буде виведено повідомлення про помилку.

```php
<?php

$file = 'some_file';

if (posix_eaccess($file, POSIX_R_OK | POSIX_W_OK)) {
    echo 'Файл доступен для чтения и записи!';

} else {
    $error = posix_get_last_error();

    echo "Ошибка $error: " . posix_strerror($error);
}

?>
```

### Примітки

### Дивіться також

-   [posix\_get\_last\_error()](function.posix-get-last-error.md) \- Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею
-   [posix\_strerror()](function.posix-strerror.md) \- Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки
-   [posix\_access()](function.posix-access.md) \- Визначає доступність файлу
