---
navigation:
  - class.swoole-atomic.md: « Swoole\\Atomic
  - swoole-atomic.cmpset.md: 'Swoole\\Atomic::cmpset »'
  - index.md: PHP Manual
  - class.swoole-atomic.md: Swoole\\Atomic
title: 'Swoole\\Atomic::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Atomic::add

(PECL swoole >= 1.9.0)

Swoole\\Atomic::add — Додає число значення атомарного об'єкта

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
