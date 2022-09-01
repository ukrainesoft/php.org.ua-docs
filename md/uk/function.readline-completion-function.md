---
navigation:
  - function.readline-clear-history.html: « readlineclearhistory
  - function.readline-info.html: readlineinfo »
  - index.md: PHP Manual
  - ref.readline.md: Функции Readline
title: readlinecompletionfunction
---
# readlinecompletionfunction

(PHP 4, PHP 5, PHP 7, PHP 8)

readlinecompletionfunction — Зареєструвати функцію автодоповнення

### Опис

```methodsynopsis
readline_completion_function(callable $callback): bool
```

Функція реєструє автодоповнення. Це те саме, як якщо ви натискаєте табуляцію в Bash і рядок доповнюється найбільш відповідним текстом.

### Список параметрів

`callback`

Ім'я функції, яка приймає рядок та повертає масив відповідних збігів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
