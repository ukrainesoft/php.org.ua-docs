---
navigation:
  - function.stream-wrapper-register.html: « streamwrapperregister
  - function.stream-wrapper-unregister.html: streamwrapperunregister »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamwrapperrestore
---
# streamwrapperrestore

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamwrapperrestore — Відновлює скасовану вбудовану обгортку.

### Опис

```methodsynopsis
stream_wrapper_restore(string $protocol): bool
```

Відновлює вбудовану обгортку, реєстрацію якої раніше було скасовано за допомогою [streamwrapperunregister()](function.stream-wrapper-unregister.md)

### Список параметрів

`protocol`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
