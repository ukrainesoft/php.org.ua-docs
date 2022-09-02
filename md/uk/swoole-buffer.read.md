---
navigation:
  - swoole-buffer.expand.md: '« SwooleBuffer::expand'
  - swoole-buffer.recycle.md: 'SwooleBuffer::recycle »'
  - index.md: PHP Manual
  - class.swoole-buffer.md: SwooleBuffer
title: 'SwooleBuffer::read'
---
# SwooleBuffer::read

(PECL swoole >= 1.9.0)

SwooleBuffer::read — Читає дані з буфера пам'яті на основі зміщення та довжини

### Опис

```methodsynopsis
public Swoole\Buffer::read(int $offset, int $length): string
```

### Список параметрів

`offset`

Зміщення.

`length`

довжина.

### Значення, що повертаються

Дані, зчитані з буфера пам'яті.
