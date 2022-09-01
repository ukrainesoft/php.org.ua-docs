---
navigation:
  - limititerator.current.md: '« LimitIterator::current'
  - limititerator.getposition.md: 'LimitIterator::getPosition »'
  - index.md: PHP Manual
  - class.limititerator.md: LimitIterator
title: 'LimitIterator::getInnerIterator'
---
# LimitIterator::getInnerIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

LimitIterator::getInnerIterator — Отримання внутрішнього об'єкта-ітератора

### Опис

```methodsynopsis
public LimitIterator::getInnerIterator(): Iterator
```

Повертає об'єкт-ітератор [Iterator](class.iterator.md) приховані всередині об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Внутрішній об'єкт-ітератор, переданий конструктору [LimitIterator::construct()](limititerator.construct.md)

### Дивіться також

-   [LimitIterator::construct()](limititerator.construct.md) - Конструктор класу LimitIterator
-   [IteratorIterator::getInnerIterator()](iteratoriterator.getinneriterator.md) - отримує внутрішній ітератор
