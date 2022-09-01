---
navigation:
  - parallel-channel.send.html: '« parallelChannel::send'
  - class.parallel-events.html: parallelEvents »
  - index.md: PHP Manual
  - class.parallel-channel.html: parallelChannel
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
