---
navigation:
  - parallel-runtime.close.html: '« parallelRuntime::close'
  - class.parallel-future.html: parallelFuture »
  - index.md: PHP Manual
  - class.parallel-runtime.html: parallelRuntime
title: 'parallelRuntime::kill'
---
# parallelRuntime::kill

parallelRuntime::kill — З'єднання під час виконання

### Опис

```methodsynopsis
public parallel\Runtime::kill(): void
```

Намагається примусово завершити роботу середовища виконання.

> **Зауваження**
> 
> Заплановані для виконання завдання не будуть виконані, поточне завдання буде перервано.

**Увага**

Внутрішні виклики функцій не можуть бути перервані.

### Помилки

**Увага**

Викидає parallelRuntimeErrorClosed, якщо Runtime вже було закрито.
