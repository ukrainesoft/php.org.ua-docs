---
navigation:
  - spldoublylinkedlist.offsetset.md: '« SplDoublyLinkedList::offsetSet'
  - spldoublylinkedlist.pop.md: 'SplDoublyLinkedList::pop »'
  - index.md: PHP Manual
  - class.spldoublylinkedlist.md: SplDoublyLinkedList
title: 'SplDoublyLinkedList::offsetUnset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplDoublyLinkedList::offsetUnset

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplDoublyLinkedList::offsetUnset — Видаляє значення за вказаним індексом $index

### Опис

```methodsynopsis
public SplDoublyLinkedList::offsetUnset(int $index): void
```

Видаляє значення за вказаним індексом.

### Список параметрів

`index`

Індекс, котрій видаляється значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md), когда`index` виходить за межі, або коли `index` може бути представлений як цілого числа.
