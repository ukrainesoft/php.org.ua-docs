---
navigation:
  - parallel-events.setinput.html: '« parallelEvents::setInput'
  - parallel-events.addfuture.html: 'parallelEvents::addFuture »'
  - index.md: PHP Manual
  - class.parallel-events.html: parallelEvents
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
