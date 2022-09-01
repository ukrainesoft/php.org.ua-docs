---
navigation:
  - parallel-events.addchannel.html: '« parallelEvents::addChannel'
  - parallel-events.remove.html: 'parallelEvents::remove »'
  - index.html: PHP Manual
  - class.parallel-events.html: parallelEvents
title: 'parallelEvents::addFuture'
---
# parallelEvents::addFuture

parallelEvents::addFuture — Цілі

### Опис

```methodsynopsis
public parallel\Events::addFuture(string $name, parallel\Future $future): void
```

Стежить за подіями у заданому `future`

### Помилки

**Увага**

Викидає parallelEventsErrorExistence, якщо ціль з даним ім'ям вже був доданий.
