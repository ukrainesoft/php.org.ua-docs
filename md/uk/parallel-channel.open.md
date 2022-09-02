---
navigation:
  - parallel-channel.make.md: '« parallelChannel::make'
  - parallel-channel.recv.md: 'parallelChannel::recv »'
  - index.md: PHP Manual
  - class.parallel-channel.md: parallelChannel
title: 'parallelChannel::open'
---
# parallelChannel::open

parallelChannel::open — Доступ

### Опис

```methodsynopsis
public parallel\Channel::open(string $name): Channel
```

Відкриває канал із заданим ім'ям

### Помилки

**Увага**

Викидає parallelChannelErrorЯкщо канал не існує.
