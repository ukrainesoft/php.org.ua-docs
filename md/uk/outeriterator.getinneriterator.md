---
navigation:
  - class.outeriterator.md: « OuterIterator
  - class.recursiveiterator.md: RecursiveIterator »
  - index.md: PHP Manual
  - class.outeriterator.md: OuterIterator
title: 'OuterIterator::getInnerIterator'
---
# OuterIterator::getInnerIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

OuterIterator::getInnerIterator — Повертає внутрішній ітератор для поточного елемента

### Опис

```methodsynopsis
public OuterIterator::getInnerIterator(): ?Iterator
```

Повертає внутрішній ітератор поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Внутрішній ітератор для поточного елемента, якщо він існує або **`null`** в іншому випадку.
