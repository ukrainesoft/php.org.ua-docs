---
navigation:
  - parallel-runtime.close.md: '« parallel\\Runtime::close'
  - class.parallel-future.md: parallel\\Future »
  - index.md: PHP Manual
  - class.parallel-runtime.md: parallel\\Runtime
title: 'parallel\\Runtime::kill'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Runtime::kill

(0.8.0)

parallel\\Runtime::kill — З'єднання під час виконання

### Опис

```methodsynopsis
public parallel\Runtime::kill(): void
```

Намагається примусово завершити роботу середовища виконання.

> **Зауваження** :
> 
> Заплановані для виконання завдання не будуть виконані, поточне завдання буде перервано.

**Увага**

Внутрішні виклики функцій не можуть бути перервані.

### Помилки

**Увага**

Викидає parallel\\Runtime\\Error\\Closed, якщо Runtime вже було закрито.
