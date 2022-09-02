---
navigation:
  - splqueue.construct.md: '« SplQueue::construct'
  - splqueue.enqueue.md: 'SplQueue::enqueue »'
  - index.md: PHP Manual
  - class.splqueue.md: SplQueue
title: 'SplQueue::dequeue'
---
# SplQueue::dequeue

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplQueue::dequeue — Видаляє елемент із черги

### Опис

```methodsynopsis
public SplQueue::dequeue(): mixed
```

Видаляє `value` із початку черги.

> **Зауваження**
> 
> **SplQueue::dequeue()** - псевдонім [SplDoublyLinkedList::shift()](spldoublylinkedlist.shift.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення видаленого із черги елемента.
