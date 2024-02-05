---
navigation:
  - parallel-events.addfuture.md: '« parallel\\Events::addFuture'
  - parallel-events.poll.md: 'parallel\\Events::poll »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallel\\Events
title: 'parallel\\Events::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events::remove

(0.9.0)

parallel\\Events::remove — Цілі

### Опис

```methodsynopsis
public parallel\Events::remove(string $target): void
```

Видаляє заданий `target`

### Помилки

**Увага**

Викидає parallel\\Events\\Error\\Existence, якщо ціль із зазначеним ім'ям не знайдена.
