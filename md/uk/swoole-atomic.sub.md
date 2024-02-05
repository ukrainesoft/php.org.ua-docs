---
navigation:
  - swoole-atomic.set.md: '« Swoole\\Atomic::set'
  - class.swoole-buffer.md: Swoole\\Buffer »
  - index.md: PHP Manual
  - class.swoole-atomic.md: Swoole\\Atomic
title: 'Swoole\\Atomic::sub'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Atomic::sub

(PECL swoole >= 1.9.0)

Swoole\\Atomic::sub — Віднімає число із значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::sub(int $sub_value = ?): int
```

Віднімає число значення атомарного об'єкта.

### Список параметрів

`sub_value`

Значення, яке буде віднято від поточного значення.

### Значення, що повертаються

Поточне значення атомного об'єкта.
