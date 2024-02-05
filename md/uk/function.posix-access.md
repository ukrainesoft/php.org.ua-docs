---
navigation:
  - ref.posix.md: « POSIX Функції
  - function.posix-ctermid.md: posix\_ctermid »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_access
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_access

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

posix\_access — Визначає доступність файлу

### Опис

```methodsynopsis
posix_access(string $filename, int $flags = 0): bool
```

Функция\*\*posix\_access()\*\*проверяет права пользователя на доступ к файлу.

### Список параметрів

`filename`

Шлях до файлу, що перевіряється.

`flags`

Маска, що складається з однієї або більше констант: **`POSIX_F_OK`** **`POSIX_R_OK`** **`POSIX_W_OK`** або **`POSIX_X_OK`**

**`POSIX_R_OK`** **`POSIX_W_OK`** і **`POSIX_X_OK`** перевіряють існування та доступність файлу на читання, запис та виконання . **`POSIX_F_OK`** перевіряє лише існування файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** posix\_access()\*\*\*\*

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

-   [posix\_get\_last\_error()](function.posix-get-last-error.md) \- Повертає номер помилки, що сталася в останній posix функції, що завершилася невдачею
-   [posix\_strerror()](function.posix-strerror.md) \- Повертає системне повідомлення про помилку, ґрунтуючись на отриманому номері помилки
