---
navigation:
  - swoole-atomic.set.html: '« SwooleAtomic::set'
  - class.swoole-buffer.html: SwooleBuffer »
  - index.md: PHP Manual
  - class.swoole-atomic.html: SwooleAtomic
title: 'SwooleAtomic::sub'
---
# SwooleAtomic::sub

(PECL swoole >= 1.9.0)

SwooleAtomic::sub — Віднімає число із значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::sub(int $sub_value = ?): int
```

Віднімає число із значення атомарного об'єкта.

### Список параметрів

`sub_value`

Значення, яке буде віднято від поточного значення.

### Значення, що повертаються

Поточне значення атомного об'єкта.
