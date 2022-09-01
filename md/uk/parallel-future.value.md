---
navigation:
  - parallel-future.done.html: '« parallelFuture::done'
  - class.parallel-channel.html: parallelChannel »
  - index.html: PHP Manual
  - class.parallel-future.html: parallelFuture
title: 'parallelFuture::value'
---
# parallelFuture::value

parallelFuture::value — Дозвіл

### Опис

```methodsynopsis
public parallel\Future::value(): mixed
```

Повертає (і за потреби чекає) повернення із завдання.

### Винятки

**Увага**

Викидає parallelFutureError, якщо очікування не вдалося (внутрішня помилка).

**Увага**

Викидає parallelFutureErrorKilled, якщо [parallelRuntime](class.parallel-runtime.html) виконання завдання було перервано.

**Увага**

Викидає parallelFutureErrorCancelled, якщо завдання було скасовано.

**Увага**

Викидає parallelFutureErrorForeign, якщо завдання викликало нерозпізнане неперехоплене виняток.

**Увага**

Викидає [Throwable](class.throwable.html), не спіймані у завданні.
