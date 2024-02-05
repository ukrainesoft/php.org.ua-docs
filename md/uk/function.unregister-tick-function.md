---
navigation:
  - function.register-tick-function.md: « register\_tick\_function
  - book.quickhash.md: Quickhash »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: unregister\_tick\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# unregister\_tick\_function

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

unregister\_tick\_function — Видалення функції зі списку зареєстрованих для виконання на кожному тику

### Опис

```methodsynopsis
unregister_tick_function(callable $callback): void
```

Видаляє callback-функцію, передану параметр `callback` зі списку функцій, так що вона більше не виконується при кожному тику (дивіться [tick](control-structures.declare.md)

### Список параметрів

`callback`

Функція, що видаляється.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [register\_tick\_function()](function.register-tick-function.md) \- Реєструє функцію для виконання при кожному тику
