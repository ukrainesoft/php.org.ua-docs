---
navigation:
  - parallel-channel.recv.html: '« parallelChannel::recv'
  - parallel-channel.close.html: 'parallelChannel::close »'
  - index.md: PHP Manual
  - class.parallel-channel.html: parallelChannel
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
