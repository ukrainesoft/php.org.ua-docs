---
navigation:
  - class.iteratoraggregate.md: « IteratorAggregate
  - class.throwable.md: Throwable »
  - index.md: PHP Manual
  - class.iteratoraggregate.md: IteratorAggregate
title: 'IteratorAggregate::getIterator'
---
# IteratorAggregate::getIterator

(PHP 5, PHP 7, PHP 8)

IteratorAggregate::getIterator — Отримує зовнішній ітератор

### Опис

```methodsynopsis
public IteratorAggregate::getIterator(): Traversable
```

Повертає зовнішній ітератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр об'єкта, що реалізує [Iterator](class.iterator.md) або [Traversable](class.traversable.md)

### Помилки

Викидає виняток [Exception](class.exception.md) у разі виникнення помилки.
