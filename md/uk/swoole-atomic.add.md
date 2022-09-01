---
navigation:
  - class.swoole-atomic.html: « SwooleAtomic
  - swoole-atomic.cmpset.html: 'SwooleAtomic::cmpset »'
  - index.html: PHP Manual
  - class.swoole-atomic.html: SwooleAtomic
title: 'SwooleAtomic::add'
---
# SwooleAtomic::add

(PECL swoole >= 1.9.0)

SwooleAtomic::add — Додає число значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::add(int $add_value = ?): int
```

Додає число значення атомарного об'єкта.

### Список параметрів

`add_value`

Значення, яке буде додано до поточного значення.

### Значення, що повертаються

Нове значення атомарного об'єкта.
