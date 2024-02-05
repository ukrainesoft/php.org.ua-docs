---
navigation:
  - parallel-channel.open.md: '« parallel\\Channel::open'
  - parallel-channel.send.md: 'parallel\\Channel::send »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallel\\Channel
title: 'parallel\\Channel::recv'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Channel::recv

(0.9.0)

parallel\\Channel::recv — Спільне використання

### Опис

```methodsynopsis
public parallel\Channel::recv(): mixed
```

Отримує значення з цього каналу

### Помилки

**Увага**

Викидає parallel\\Channel\\Error\\Closed, якщо канал закритий.
