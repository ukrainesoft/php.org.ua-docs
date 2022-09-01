---
navigation:
  - throwable.getline.md: '« Throwable::getLine'
  - throwable.gettraceasstring.md: 'Throwable::getTraceAsString »'
  - index.md: PHP Manual
  - class.throwable.md: Throwable
title: 'Throwable::getTrace'
---
# Throwable::getTrace

(PHP 7, PHP 8)

Throwable::getTrace — Повертає трасування стека

### Опис

```methodsynopsis
public Throwable::getTrace(): array
```

Повертає трасування стека у вигляді масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає трасування стека у вигляді масиву в такому ж форматі, що й [debugbacktrace()](function.debug-backtrace.html)

### Дивіться також

-   [Exception::getTrace()](exception.gettrace.md) - Отримує трасування стека
