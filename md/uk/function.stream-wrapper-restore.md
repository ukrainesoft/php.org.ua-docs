---
navigation:
  - function.stream-wrapper-register.md: « stream\_wrapper\_register
  - function.stream-wrapper-unregister.md: stream\_wrapper\_unregister »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_wrapper\_restore
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_wrapper\_restore

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

stream\_wrapper\_restore — Відновлює скасовану вбудовану обгортку.

### Опис

```methodsynopsis
stream_wrapper_restore(string $protocol): bool
```

Відновлює вбудовану обгортку, реєстрацію якої раніше було скасовано за допомогою [stream\_wrapper\_unregister()](function.stream-wrapper-unregister.md)

### Список параметрів

`protocol`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
