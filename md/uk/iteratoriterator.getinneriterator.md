---
navigation:
  - iteratoriterator.current.html: '« IteratorIterator::current'
  - iteratoriterator.key.html: 'IteratorIterator::key »'
  - index.html: PHP Manual
  - class.iteratoriterator.html: IteratorIterator
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

Внутрішній ітератор, який було передано методу [IteratorIterator::construct()](iteratoriterator.construct.html) або \*\*`null`\*\*якщо внутрішній ітератор відсутній.

### Дивіться також

-   [Iterator](class.iterator.html)
-   [OuterIterator](class.outeriterator.html)
