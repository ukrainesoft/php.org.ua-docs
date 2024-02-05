---
navigation:
  - spldoublylinkedlist.offsetexists.md: '« SplDoublyLinkedList::offsetExists'
  - spldoublylinkedlist.offsetset.md: 'SplDoublyLinkedList::offsetSet »'
  - index.md: PHP Manual
  - class.spldoublylinkedlist.md: SplDoublyLinkedList
title: 'SplDoublyLinkedList::offsetGet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplDoublyLinkedList::offsetGet

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplDoublyLinkedList::offsetGet — Повертає значення за вказаним індексом

### Опис

```methodsynopsis
public SplDoublyLinkedList::offsetGet(int $index): mixed
```

### Список параметрів

`index`

Індекс.

### Значення, що повертаються

Значення зазначеного індексу `index`

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md), когда`index` виходить за межі, або коли `index` може бути представлений як цілого числа.
