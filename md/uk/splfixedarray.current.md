---
navigation:
  - splfixedarray.count.md: '« SplFixedArray::count'
  - splfixedarray.fromarray.md: 'SplFixedArray::fromArray »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::current'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::current

(PHP 5 >= 5.3.0, PHP 7)

SplFixedArray::current — Повертає поточний елемент масиву

### Опис

```methodsynopsis
public SplFixedArray::current(): mixed
```

Отримує поточний елемент масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний елемент масиву.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md)коли внутрішній покажчик масиву вказує на неправильний індекс або вийшов за допустимі межі.
