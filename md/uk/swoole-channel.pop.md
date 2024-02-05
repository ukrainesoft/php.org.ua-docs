---
navigation:
  - swoole-channel.destruct.md: '« Swoole\\Channel::\_\_destruct'
  - swoole-channel.push.md: 'Swoole\\Channel::push »'
  - index.md: PHP Manual
  - class.swoole-channel.md: Swoole\\Channel
title: 'Swoole\\Channel::pop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Channel::pop

(PECL swoole >= 1.9.0)

Swoole\\Channel::pop — Читає та витягує дані з каналу Swoole

### Опис

```methodsynopsis
public Swoole\Channel::pop(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо канал порожній, функція поверне false чи несеріалізовані дані.
