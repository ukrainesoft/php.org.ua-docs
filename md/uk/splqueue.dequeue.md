---
navigation:
  - class.splqueue.md: « SplQueue
  - splqueue.enqueue.md: 'SplQueue::enqueue »'
  - index.md: PHP Manual
  - class.splqueue.md: SplQueue
title: 'SplQueue::dequeue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplQueue::dequeue

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplQueue::dequeue — Видаляє елемент із черги

### Опис

```methodsynopsis
public SplQueue::dequeue(): mixed
```

Видаляє `value`из начала очереди.

> **Зауваження** :
> 
> \*\*SplQueue::dequeue()\*\*- псевдоним[SplDoublyLinkedList::shift()](spldoublylinkedlist.shift.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення видаленого із черги елемента.
