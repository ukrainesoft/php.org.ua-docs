---
navigation:
  - splqueue.dequeue.md: '« SplQueue::dequeue'
  - splqueue.setiteratormode.md: 'SplQueue::setIteratorMode »'
  - index.md: PHP Manual
  - class.splqueue.md: SplQueue
title: 'SplQueue::enqueue'
---
# SplQueue::enqueue

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplQueue::enqueue — Додає елемент до черги

### Опис

```methodsynopsis
public SplQueue::enqueue(mixed $value): void
```

Додає `value` на кінець черги.

> **Зауваження**
> 
> **SplQueue::enqueue()** - псевдонім [SplDoublyLinkedList::push()](spldoublylinkedlist.push.md)

### Список параметрів

`value`

Значення для постановки на чергу.

### Значення, що повертаються

Функція не повертає значення після виконання.
