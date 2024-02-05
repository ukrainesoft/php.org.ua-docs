---
navigation:
  - swoole-buffer.expand.md: '« Swoole\\Buffer::expand'
  - swoole-buffer.recycle.md: 'Swoole\\Buffer::recycle »'
  - index.md: PHP Manual
  - class.swoole-buffer.md: Swoole\\Buffer
title: 'Swoole\\Buffer::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Buffer::read

(PECL swoole >= 1.9.0)

Swoole\\Buffer::read — Читає дані з буфера пам'яті на основі зміщення та довжини

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
