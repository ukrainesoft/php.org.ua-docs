---
navigation:
  - swoole-channel.destruct.md: '« SwooleChannel::destruct'
  - swoole-channel.push.md: 'SwooleChannel::push »'
  - index.md: PHP Manual
  - class.swoole-channel.md: SwooleChannel
title: 'SwooleChannel::pop'
---
# SwooleChannel::pop

(PECL swoole >= 1.9.0)

SwooleChannel::pop — Читає та витягує дані з каналу Swoole

### Опис

```methodsynopsis
public Swoole\Channel::pop(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо канал порожній, функція поверне false чи несеріалізовані дані.
