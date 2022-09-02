---
navigation:
  - parallel-events.setinput.md: '« parallelEvents::setInput'
  - parallel-events.addfuture.md: 'parallelEvents::addFuture »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallelEvents
title: 'parallelEvents::addChannel'
---
# parallelEvents::addChannel

parallelEvents::addChannel — Цілі

### Опис

```methodsynopsis
public parallel\Events::addChannel(parallel\Channel $channel): void
```

Стежить за подіями у заданому `channel`

### Помилки

**Увага**

Викидає parallelEventsErrorExistence, якщо канал вже було додано.
