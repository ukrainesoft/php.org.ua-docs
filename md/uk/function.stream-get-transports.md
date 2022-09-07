---
navigation:
  - function.stream-get-meta-data.md: « streamgetmetadata
  - function.stream-get-wrappers.md: streamgetwrappers »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamgettransports
---
# streamgettransports

(PHP 5, PHP 7, PHP 8)

streamgettransports — Отримати список зареєстрованих транспортів сокету

### Опис

```methodsynopsis
stream_get_transports(): array
```

Повертає індексований масив, який містить назви всіх транспортів сокету, доступних на запущеній системі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає індексований масив назв транспорту сокету.

### Приклади

**Приклад #1 Приклад використання **streamgettransports()****

```php
<?php
$xportlist = stream_get_transports();
print_r($xportlist);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array (
  [0] => tcp
  [1] => udp
  [2] => unix
  [3] => udg
)
```

### Дивіться також

-   [streamgetfilters()](function.stream-get-filters.md) - Отримати список зареєстрованих фільтрів
-   [streamgetwrappers()](function.stream-get-wrappers.md) - Отримати список зареєстрованих потоків
