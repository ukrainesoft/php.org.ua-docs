---
navigation:
  - class.parallel-future.html: « parallelFuture
  - parallel-future.cancelled.html: 'parallelFuture::cancelled »'
  - index.md: PHP Manual
  - class.parallel-future.html: parallelFuture
title: 'parallelFuture::cancel'
---
# parallelFuture::cancel

parallelFuture::cancel — Припинення

### Опис

```methodsynopsis
public parallel\Future::cancel(): bool
```

Намагається перервати завдання.

> **Зауваження**
> 
> Якщо завдання запущено, його буде перервано.

**Увага**

Внутрішні виклики функцій не можуть бути перервані.

### Винятки

**Увага**

Викидає parallelFutureErrorKilled, якщо [parallelRuntime](class.parallel-runtime.html) виконання завдання було перервано.

**Увага**

Викидає parallelFutureErrorCancelled, якщо завдання вже перервано.
