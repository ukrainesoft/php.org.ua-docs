---
navigation:
  - spldoublylinkedlist.offsetexists.html: '« SplDoublyLinkedList::offsetExists'
  - spldoublylinkedlist.offsetset.html: 'SplDoublyLinkedList::offsetSet »'
  - index.html: PHP Manual
  - class.spldoublylinkedlist.html: SplDoublyLinkedList
title: 'SplDoublyLinkedList::offsetGet'
---
# SplDoublyLinkedList::offsetGet

(PHP 5> = 5.3.0, PHP 7, PHP 8)

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

Викидає виняток [OutOfRangeException](class.outofrangeexception.html), коли `index` виходить за межі, або коли `index` може бути представлений як цілого числа.
