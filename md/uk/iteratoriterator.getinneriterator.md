---
navigation:
  - iteratoriterator.current.md: '« IteratorIterator::current'
  - iteratoriterator.key.md: 'IteratorIterator::key »'
  - index.md: PHP Manual
  - class.iteratoriterator.md: IteratorIterator
title: 'IteratorIterator::getInnerIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IteratorIterator::getInnerIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

IteratorIterator::getInnerIterator — Отримує внутрішній ітератор

### Опис

```methodsynopsis
public IteratorIterator::getInnerIterator(): ?Iterator
```

Отримує внутрішній ітератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Внутрішній ітератор, який було передано методу [IteratorIterator::\_\_construct()](iteratoriterator.construct.md)или\*\*`null`\*\*якщо внутрішній ітератор відсутній.

### Дивіться також

-   [Iterator](class.iterator.md)
-   [OuterIterator](class.outeriterator.md)
