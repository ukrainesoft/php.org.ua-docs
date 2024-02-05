---
navigation:
  - function.stream-get-transports.md: « stream\_get\_transports
  - function.stream-is-local.md: stream\_is\_local »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_get\_wrappers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_get\_wrappers

(PHP 5, PHP 7, PHP 8)

stream\_get\_wrappers — Отримати список зареєстрованих потоків

### Опис

```methodsynopsis
stream_get_wrappers(): array
```

Витягує список зареєстрованих потоків, доступних на запущеній системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив, що містить назви всіх обертів потоків, доступних на запущеній системі.

### Приклади

**Пример #1 Пример использования**stream\_get\_wrappers()\*\*\*\*

```php
<?php
print_r(stream_get_wrappers());
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [stream\_wrapper\_register()](function.stream-wrapper-register.md) \- реєструє обгортку URL, реалізовану у вигляді PHP-класу
