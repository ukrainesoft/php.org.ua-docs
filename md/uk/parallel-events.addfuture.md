---
navigation:
  - parallel-events.addchannel.md: '« parallel\\Events::addChannel'
  - parallel-events.remove.md: 'parallel\\Events::remove »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallel\\Events
title: 'parallel\\Events::addFuture'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events::addFuture

(0.9.0)

parallel\\Events::addFuture — Цілі

### Опис

```methodsynopsis
public parallel\Events::addFuture(string $name, parallel\Future $future): void
```

Стежить за подіями у заданому `future`

### Помилки

**Увага**

Викидає parallel\\Events\\Error\\Existence, якщо ціль з даним ім'ям вже був доданий.
