---
navigation:
  - parallel-channel.recv.md: '« parallel\\Channel::recv'
  - parallel-channel.close.md: 'parallel\\Channel::close »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallel\\Channel
title: 'parallel\\Channel::send'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Channel::send

(0.9.0)

parallel\\Channel::send — Спільне використання

### Опис

```methodsynopsis
public parallel\Channel::send(mixed $value): void
```

Відправляє задане значення каналу

### Помилки

**Увага**

Викидає parallel\\Channel\\Error\\Closed, якщо канал закритий.

**Увага**

Викидає parallel\\Channel\\Error\\Ilegallegal, якщо значення неприпустимо.
