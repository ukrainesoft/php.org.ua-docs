---
navigation:
  - class.parallel-future.md: « parallel\\Future
  - parallel-future.cancelled.md: 'parallel\\Future::cancelled »'
  - index.md: PHP Manual
  - class.parallel-future.md: parallel\\Future
title: 'parallel\\Future::cancel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Future::cancel

(0.9.0)

parallel\\Future::cancel — Припинення

### Опис

```methodsynopsis
public parallel\Future::cancel(): bool
```

Намагається перервати завдання.

> **Зауваження** :
> 
> Якщо завдання запущено, його буде перервано.

**Увага**

Внутрішні виклики функцій не можуть бути перервані.

### Винятки

**Увага**

Викидає parallel\\Future\\Error\\Killed, если[parallel\\Runtime](class.parallel-runtime.md) виконання завдання було перервано.

**Увага**

Викидає parallel\\Future\\Error\\Cancelled, якщо завдання вже перервано.
