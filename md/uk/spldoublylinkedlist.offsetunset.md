---
navigation:
  - spldoublylinkedlist.offsetset.html: '« SplDoublyLinkedList::offsetSet'
  - spldoublylinkedlist.pop.html: 'SplDoublyLinkedList::pop »'
  - index.html: PHP Manual
  - class.spldoublylinkedlist.html: SplDoublyLinkedList
title: 'SplDoublyLinkedList::offsetUnset'
---
# SplDoublyLinkedList::offsetUnset

(PHP 5> = 5.3.0, PHP 7, PHP 8)

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

Викидає виняток [OutOfRangeException](class.outofrangeexception.html), коли `index` виходить за межі, або коли `index` може бути представлений як цілого числа.
