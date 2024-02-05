---
navigation:
  - swoole-atomic.add.md: '« Swoole\\Atomic::add'
  - swoole-atomic.construct.md: 'Swoole\\Atomic::\_\_construct »'
  - index.md: PHP Manual
  - class.swoole-atomic.md: Swoole\\Atomic
title: 'Swoole\\Atomic::cmpset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Atomic::cmpset

(PECL swoole >= 1.9.0)

Swoole\\Atomic::cmpset — Порівнює та встановлює значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::cmpset(int $cmp_value, int $new_value): int
```

### Список параметрів

`cmp_value`

Значення порівняння з поточним значенням атомарного об'єкта.

`new_value`

Значення для атомарного об'єкта, якщо значення cmp\_value збігається із поточним значенням атомарного об'єкта.

### Значення, що повертаються

Нове значення атомарного об'єкта.
