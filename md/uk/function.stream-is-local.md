---
navigation:
  - function.stream-get-wrappers.md: « stream\_get\_wrappers
  - function.stream-isatty.md: stream\_isatty »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_is\_local
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_is\_local

(PHP 5 >= 5.2.4, PHP 7, PHP 8)

stream\_is\_local — Перевіряє, чи потік є локальним потоком.

### Опис

```methodsynopsis
stream_is_local(resource|string $stream): bool
```

Перевіряє, чи потік або URL локальний чи ні.

### Список параметрів

`stream`

Ресурс потоку або URL для перевірки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад виконання** stream\_is\_local()\*\*\*\*

Приклад простого використання.

```php
<?php
var_dump(stream_is_local("http://example.com"));
var_dump(stream_is_local("/etc"));
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
bool(true)
```
