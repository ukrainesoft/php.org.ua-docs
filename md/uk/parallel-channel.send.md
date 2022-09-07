---
navigation:
  - parallel-channel.recv.md: '« parallelChannel::recv'
  - parallel-channel.close.md: 'parallelChannel::close »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallelChannel
title: 'parallelChannel::send'
---
# parallelChannel::send

parallelChannel::send — Спільне використання

### Опис

```methodsynopsis
public parallel\Channel::send(mixed $value): void
```

Відправляє задане значення каналу

### Помилки

**Увага**

Викидає parallelChannelErrorClosed, якщо канал закритий.

**Увага**

Викидає parallelChannelErrorIlegallegal, якщо значення неприпустимо.
