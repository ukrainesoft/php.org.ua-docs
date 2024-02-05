---
navigation:
  - parallel-channel.send.md: '« parallel\\Channel::send'
  - class.parallel-events.md: parallel\\Events »
  - index.md: PHP Manual
  - class.parallel-channel.md: parallel\\Channel
title: 'parallel\\Channel::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Channel::close

(0.9.0)

parallel\\Channel::close — Закриття

### Опис

```methodsynopsis
public parallel\Channel::close(): void
```

Закриває канал.

### Помилки

**Увага**

Викидає parallel\\Channel\\Error\\Closed, якщо канал вже був закритий.
