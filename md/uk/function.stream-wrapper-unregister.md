---
navigation:
  - function.stream-wrapper-restore.md: « stream\_wrapper\_restore
  - book.swoole.md: Swoole »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_wrapper\_unregister
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_wrapper\_unregister

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

stream\_wrapper\_unregister — Скасує реєстрацію обгортки URL

### Опис

```methodsynopsis
stream_wrapper_unregister(string $protocol): bool
```

Дозволяє вам вимкнути вже певну обгортку потоку. Як тільки обгортка буде вимкнена, ви можете перезаписати її обгорткою користувача, використовуючи [stream\_wrapper\_register()](function.stream-wrapper-register.md) або включити її повторно, використовуючи [stream\_wrapper\_restore()](function.stream-wrapper-restore.md)

### Список параметрів

`protocol`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
