---
navigation:
  - domnodelist.count.md: '« DOMNodeList::count'
  - domnodelist.item.md: 'DOMNodeList::item »'
  - index.md: PHP Manual
  - class.domnodelist.md: DOMNodeList
title: 'DOMNodeList::getIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNodeList::getIterator

(PHP 8)

DOMNodeList::getIterator — Отримує зовнішній ітератор

### Опис

```methodsynopsis
public DOMNodeList::getIterator(): Iterator
```

Повертає зовнішній ітератор до списку вузлів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр об'єкта, що реалізує [Iterator](class.iterator.md) або [Traversable](class.traversable.md)

### Помилки

Викидає виняток [Exception](class.exception.md)в случае возникновения ошибки.

### Дивіться також

-   [IteratorAggregate::getIterator()](iteratoraggregate.getiterator.md) \- отримує зовнішній ітератор
