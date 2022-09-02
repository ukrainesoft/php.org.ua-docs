---
navigation:
  - parallel-channel.send.md: '« parallelChannel::send'
  - class.parallel-events.md: parallelEvents »
  - index.md: PHP Manual
  - class.parallel-channel.md: parallelChannel
title: 'parallelChannel::close'
---
# parallelChannel::close

parallelChannel::close — Закриття

### Опис

```methodsynopsis
public parallel\Channel::close(): void
```

Закриває канал.

### Помилки

**Увага**

Викидає parallelChannelErrorClosed, якщо канал вже був закритий.
