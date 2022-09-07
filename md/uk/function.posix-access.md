---
navigation:
  - ref.posix.md: « POSIX Функции
  - function.posix-ctermid.md: posixctermid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixaccess
---
# posixaccess

(PHP 5> = 5.1.0, PHP 7, PHP 8)

posixaccess — Визначає доступність файлу

### Опис

```methodsynopsis
posix_access(string $filename, int $flags = 0): bool
```

Функція **posixaccess()** перевіряє права користувача доступу до файлу.

### Список параметрів

`filename`

Шлях до файлу, що перевіряється.

`flags`

Маска, що складається з однієї або більше констант: **`POSIX_F_OK`** **`POSIX_R_OK`** **`POSIX_W_OK`** або **`POSIX_X_OK`**

**`POSIX_R_OK`** **`POSIX_W_OK`** і **`POSIX_X_OK`** перевіряють існування та доступність файлу на читання, запис та виконання . **`POSIX_F_OK`** перевіряє лише існування файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **posixaccess()****

У цьому прикладі перевіряється доступність файлу на читання та запис, інакше виводиться повідомлення про помилку.

```php
<?php

$file = 'some_file';

if (posix_access($file, POSIX_R_OK | POSIX_W_OK)) {
    echo 'Файл доступен на чтение и запись!';

} else {
    $error = posix_get_last_error();

    echo "Error $error: " . posix_strerror($error);
}

?>
```

### Примітки

### Дивіться також

-   [posixgetlasterror()](function.posix-get-last-error.md) - Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею
-   [posixstrerror()](function.posix-strerror.md) - Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки
