---
navigation:
  - parallel-events.setinput.md: '« parallel\\Events::setInput'
  - parallel-events.addfuture.md: 'parallel\\Events::addFuture »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallel\\Events
title: 'parallel\\Events::addChannel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events::addChannel

(0.9.0)

parallel\\Events::addChannel — Цілі

### Опис

```methodsynopsis
public parallel\Events::addChannel(parallel\Channel $channel): void
```

Стежить за подіями у заданому `channel`

### Помилки

**Увага**

Викидає parallel\\Events\\Error\\Existence, якщо канал вже було додано.
