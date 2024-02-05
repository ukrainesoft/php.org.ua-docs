---
navigation:
  - domnamednodemap.count.md: '« DOMNamedNodeMap::count'
  - domnamednodemap.getnameditem.md: 'DOMNamedNodeMap::getNamedItem »'
  - index.md: PHP Manual
  - class.domnamednodemap.md: DOMNamedNodeMap
title: 'DOMNamedNodeMap::getIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNamedNodeMap::getIterator

(PHP 8)

DOMNamedNodeMap::getIterator — Отримує зовнішній ітератор

### Опис

```methodsynopsis
public DOMNamedNodeMap::getIterator(): Iterator
```

Повертає зовнішній ітератор для іменованої картки вузлів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр об'єкта, що реалізує [Iterator](class.iterator.md) або [Traversable](class.traversable.md)

### Помилки

Викидає виняток [Exception](class.exception.md)в случае возникновения ошибки.

### Дивіться також

-   [IteratorAggregate::getIterator()](iteratoraggregate.getiterator.md) \- отримує зовнішній ітератор
