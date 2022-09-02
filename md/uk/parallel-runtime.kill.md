---
navigation:
  - parallel-runtime.close.md: '« parallelRuntime::close'
  - class.parallel-future.md: parallelFuture »
  - index.md: PHP Manual
  - class.parallel-runtime.md: parallelRuntime
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
