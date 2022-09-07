---
navigation:
  - parallel-events.addchannel.md: '« parallelEvents::addChannel'
  - parallel-events.remove.md: 'parallelEvents::remove »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallelEvents
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
