---
navigation:
  - closure.call.html: '« Closure::call'
  - class.generator.html: Generator »
  - index.html: PHP Manual
  - class.closure.html: Closure
title: 'Closure::fromCallable'
---
# Closure::fromCallable

(PHP 7> = 7.1.0)

Closure::fromCallable — Конвертує callable у замикання

### Опис

```methodsynopsis
public static Closure::fromCallable(callable $callback): Closure
```

Створює та повертає нову [анонимную функцию](functions.anonymous.html) із заданого `callback`, використовуючи поточну область видимості. Цей метод перевіряє, що `callback` є типом callable у поточній області видимості та викидає виняток [TypeError](class.typeerror.html), якщо це не так.

> **Зауваження**
> 
> Починаючи з PHP 8.1.0, у [Callback-функцій як об'єктів першого класу](functions.first_class_callable_syntax.html) та сама семантика, що й у цього методу.

### Список параметрів

`callback`

Об'єкт типу callable.

### Значення, що повертаються

Повертає новий об'єкт класу [Closure](class.closure.html) або викидає виняток [TypeError](class.typeerror.html), якщо `callback` не є об'єктом типу callable у поточній області видимості.

### Дивіться також

-   [Анонімні функції](functions.anonymous.html)
-   [Callback-функції як об'єкти першого класу](functions.first_class_callable_syntax.html)
