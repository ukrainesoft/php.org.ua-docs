---
navigation:
  - swoole-atomic.get.md: '« SwooleAtomic::get'
  - swoole-atomic.sub.md: 'SwooleAtomic::sub »'
  - index.md: PHP Manual
  - class.swoole-atomic.md: SwooleAtomic
title: 'SwooleAtomic::set'
---
# SwooleAtomic::set

(PECL swoole >= 1.9.0)

SwooleAtomic::set — Встановлює нове значення для атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::set(int $value): int
```

Встановлює нове значення атомарного об'єкта.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`value`

Значення для атомарного об'єкта.

### Значення, що повертаються

Поточне значення атомного об'єкта.
