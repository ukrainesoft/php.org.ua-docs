---
navigation:
  - swoole-connection-iterator.next.md: '« SwooleConnectionIterator::next'
  - swoole-connection-iterator.offsetget.md: 'SwooleConnectionIterator::offsetGet »'
  - index.md: PHP Manual
  - class.swoole-connection-iterator.md: SwooleConnectionIterator
title: 'SwooleConnectionIterator::offsetExists'
---
# SwooleConnectionIterator::offsetExists

(PECL swoole >= 1.9.0)

SwooleConnectionIterator::offsetExists — Перевіряє, чи існує зміщення

### Опис

```methodsynopsis
public Swoole\Connection\Iterator::offsetExists(int $index): bool
```

Перевіряє, чи є усунення.

### Список параметрів

`index`

Зміщення, яке потрібно перевірити.

### Значення, що повертаються

Повертає TRUE, якщо зсув існує, інакше FALSE.
