---
navigation:
  - parallel-channel.open.html: '« parallelChannel::open'
  - parallel-channel.send.html: 'parallelChannel::send »'
  - index.html: PHP Manual
  - class.parallel-channel.html: parallelChannel
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
