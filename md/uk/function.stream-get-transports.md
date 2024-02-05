---
navigation:
  - function.stream-get-meta-data.md: « stream\_get\_meta\_data
  - function.stream-get-wrappers.md: stream\_get\_wrappers »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_get\_transports
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_get\_transports

(PHP 5, PHP 7, PHP 8)

stream\_get\_transports — Отримати список зареєстрованих транспортів сокету

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

**Приклад #1 Приклад використання** stream\_get\_transports()\*\*\*\*

```php
<?php
$xportlist = stream_get_transports();
print_r($xportlist);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array (
  [0] => tcp
  [1] => udp
  [2] => unix
  [3] => udg
)
```

### Дивіться також

-   [stream\_get\_filters()](function.stream-get-filters.md) \- Отримати список зареєстрованих фільтрів
-   [stream\_get\_wrappers()](function.stream-get-wrappers.md) \- Отримати список зареєстрованих потоків
