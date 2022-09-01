---
navigation:
  - swoole-atomic.add.html: '« SwooleAtomic::add'
  - swoole-atomic.construct.html: 'SwooleAtomic::construct »'
  - index.html: PHP Manual
  - class.swoole-atomic.html: SwooleAtomic
title: 'SwooleAtomic::cmpset'
---
# SwooleAtomic::cmpset

(PECL swoole >= 1.9.0)

SwooleAtomic::cmpset — Порівнює та встановлює значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::cmpset(int $cmp_value, int $new_value): int
```

### Список параметрів

`cmp_value`

Значення порівняння з поточним значенням атомарного об'єкта.

`new_value`

Значення для атомарного об'єкта, якщо значення cmpvalue збігається із поточним значенням атомарного об'єкта.

### Значення, що повертаються

Нове значення атомарного об'єкта.
