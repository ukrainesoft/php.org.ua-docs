---
navigation:
  - parallel-runtime.run.html: '« parallelRuntime::run'
  - parallel-runtime.kill.html: 'parallelRuntime::kill »'
  - index.html: PHP Manual
  - class.parallel-runtime.html: parallelRuntime
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
