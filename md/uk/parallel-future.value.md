---
navigation:
  - parallel-future.done.md: '« parallel\\Future::done'
  - class.parallel-channel.md: parallel\\Channel »
  - index.md: PHP Manual
  - class.parallel-future.md: parallel\\Future
title: 'parallel\\Future::value'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Future::value

(0.8.0)

parallel\\Future::value — Дозвіл

### Опис

```methodsynopsis
public parallel\Future::value(): mixed
```

Повертає (і за потреби чекає) повернення із завдання.

### Винятки

**Увага**

Викидає parallel\\Future\\Error, якщо очікування не вдалося (внутрішня помилка).

**Увага**

Викидає parallel\\Future\\Error\\Killed, если[parallel\\Runtime](class.parallel-runtime.md) виконання завдання було перервано.

**Увага**

Викидає parallel\\Future\\Error\\Cancelled, якщо завдання було скасовано.

**Увага**

Викидає parallel\\Future\\Error\\Foreign, якщо завдання викликало нерозпізнане неперехоплене виняток.

**Увага**

Викидає [Throwable](class.throwable.md), не спіймані у завданні.
