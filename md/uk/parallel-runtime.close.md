---
navigation:
  - parallel-runtime.run.md: '« parallelRuntime::run'
  - parallel-runtime.kill.md: 'parallelRuntime::kill »'
  - index.md: PHP Manual
  - class.parallel-runtime.md: parallelRuntime
title: 'parallelRuntime::close'
---
# parallelRuntime::close

parallelRuntime::close — Витончене з'єднання під час виконання

### Опис

```methodsynopsis
public parallel\Runtime::close(): void
```

Запитує завершення роботи середовища виконання.

> **Зауваження**
> 
> Заплановані для виконання завдання будуть виконані до завершення роботи.

### Помилки

**Увага**

Викидає parallelRuntimeErrorClosed, якщо Runtime вже було закрито.
