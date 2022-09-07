---
navigation:
  - function.stream-get-transports.md: « streamgettransports
  - function.stream-is-local.md: streamісlocal »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamgetwrappers
---
# streamgetwrappers

(PHP 5, PHP 7, PHP 8)

streamgetwrappers — Отримати список зареєстрованих потоків

### Опис

```methodsynopsis
stream_get_wrappers(): array
```

Витягує список зареєстрованих потоків на запущеній системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив, що містить назви всіх обертів потоків, доступних на запущеній системі.

### Приклади

**Приклад #1 Приклад використання **streamgetwrappers()****

```php
<?php
print_r(stream_get_wrappers());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => php
    [1] => file
    [2] => http
    [3] => ftp
    [4] => compress.bzip2
    [5] => compress.zlib
)
```

**Приклад #2 Перевірка існування обгортки потоку**

```php
<?php
// Проверяет существование обёртки потока bzip2
if (in_array('compress.bzip2', stream_get_wrappers())) {
    echo 'compress.bzip2:// поддержка включена.';
} else {
    echo 'compress.bzip2:// поддержка не включена.';
}
?>
```

### Дивіться також

-   [streamwrapperregister()](function.stream-wrapper-register.md) - реєструє обгортку URL, реалізовану у вигляді PHP-класу
