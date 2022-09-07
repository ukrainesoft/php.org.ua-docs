---
navigation:
  - iteratoriterator.current.md: '« IteratorIterator::current'
  - iteratoriterator.key.md: 'IteratorIterator::key »'
  - index.md: PHP Manual
  - class.iteratoriterator.md: IteratorIterator
title: 'IteratorIterator::getInnerIterator'
---
# IteratorIterator::getInnerIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

IteratorIterator::getInnerIterator — Отримує внутрішній ітератор

### Опис

```methodsynopsis
public IteratorIterator::getInnerIterator(): ?Iterator
```

Отримує внутрішній ітератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Внутрішній ітератор, який було передано методу [IteratorIterator::construct()](iteratoriterator.construct.md) або \*\*`null`\*\*якщо внутрішній ітератор відсутній.

### Дивіться також

-   [Iterator](class.iterator.md)
-   [OuterIterator](class.outeriterator.md)
