---
navigation:
  - function.stream-get-contents.md: « stream\_get\_contents
  - function.stream-get-line.md: stream\_get\_line »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_get\_filters
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_get\_filters

(PHP 5, PHP 7, PHP 8)

stream\_get\_filters — Отримати список зареєстрованих фільтрів

### Опис

```methodsynopsis
stream_get_filters(): array
```

Отримати список зареєстрованих фільтрів у запущеній системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив, що містить найменування всіх доступних системних фільтрів потоку.

### Приклади

**Приклад #1 Приклад використання функції** stream\_get\_filters()\*\*\*\*

```php
<?php
$streamlist = stream_get_filters();
print_r($streamlist);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array (
  [0] => string.rot13
  [1] => string.toupper
  [2] => string.tolower
  [3] => string.base64
  [4] => string.quoted-printable
)
```

### Дивіться також

-   [stream\_filter\_register()](function.stream-filter-register.md) \- Реєструє потоковий фільтр, визначений користувачем
-   [stream\_get\_wrappers()](function.stream-get-wrappers.md) \- Отримати список зареєстрованих потоків
