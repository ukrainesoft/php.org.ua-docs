---
navigation:
  - function.readline-clear-history.md: « readline\_clear\_history
  - function.readline-info.md: readline\_info »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_completion\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_completion\_function

(PHP 4, PHP 5, PHP 7, PHP 8)

readline\_completion\_function — Зареєструвати функцію автодоповнення

### Опис

```methodsynopsis
readline_completion_function(callable $callback): bool
```

Функція реєструє автодоповнення. Це те саме, як якщо ви натискаєте табуляцію в Bash і рядок доповнюється найбільш відповідним текстом.

### Список параметрів

`callback`

Ім'я функції, яка приймає рядок та повертає масив відповідних збігів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
