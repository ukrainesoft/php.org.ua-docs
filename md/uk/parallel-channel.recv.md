---
navigation:
  - parallel-channel.open.md: '« parallelChannel::open'
  - parallel-channel.send.md: 'parallelChannel::send »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallelChannel
title: 'parallelChannel::recv'
---
# parallelChannel::recv

parallelChannel::recv — Спільне використання

### Опис

```methodsynopsis
public parallel\Channel::recv(): mixed
```

Отримує значення з цього каналу

### Помилки

**Увага**

Викидає parallelChannelErrorClosed, якщо канал закритий.
