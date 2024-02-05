---
navigation:
  - parallel-runtime.run.md: '« parallel\\Runtime::run'
  - parallel-runtime.kill.md: 'parallel\\Runtime::kill »'
  - index.md: PHP Manual
  - class.parallel-runtime.md: parallel\\Runtime
title: 'parallel\\Runtime::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Runtime::close

(0.8.0)

parallel\\Runtime::close — Витончене з'єднання під час виконання

### Опис

```methodsynopsis
public parallel\Runtime::close(): void
```

Запитує завершення роботи середовища виконання.

> **Зауваження** :
> 
> Заплановані для виконання завдання будуть виконані до завершення роботи.

### Помилки

**Увага**

Викидає parallel\\Runtime\\Error\\Closed, якщо Runtime вже було закрито.
