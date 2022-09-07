---
navigation:
  - parallel-events.addfuture.md: '« parallelEvents::addFuture'
  - parallel-events.poll.md: 'parallelEvents::poll »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallelEvents
title: 'parallelEvents::remove'
---
# parallelEvents::remove

parallelEvents::remove — Цілі

### Опис

```methodsynopsis
public parallel\Events::remove(string $target): void
```

Видаляє заданий `target`

### Помилки

**Увага**

Викидає parallelEventsErrorExistence, якщо ціль із зазначеним ім'ям не знайдена.
