---
navigation:
  - swoole-connection-iterator.offsetget.md: '« SwooleConnectionIterator::offsetGet'
  - swoole-connection-iterator.offsetunset.md: 'SwooleConnectionIterator::offsetUnset »'
  - index.md: PHP Manual
  - class.swoole-connection-iterator.md: SwooleConnectionIterator
title: 'SwooleConnectionIterator::offsetSet'
---
# SwooleConnectionIterator::offsetSet

(PECL swoole >= 1.9.0)

SwooleConnectionIterator::offsetSet — Призначає з'єднання для зазначеного усунення

### Опис

```methodsynopsis
public Swoole\Connection\Iterator::offsetSet(int $offset, mixed $connection): void
```

Призначає з'єднання для зазначеного усунення.

### Список параметрів

`offset`

Зміщення для якого призначити з'єднання.

`connection`

З'єднання для встановлення.

### Значення, що повертаються
