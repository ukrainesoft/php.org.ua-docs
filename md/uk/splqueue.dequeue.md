Видаляє елемент із черги

-   [« SplQueue::\_\_construct](splqueue.construct.html)
    
-   [SplQueue::enqueue »](splqueue.enqueue.html)
    
-   [PHP Manual](index.html)
    
-   [SplQueue](class.splqueue.html)
    
-   Видаляє елемент із черги
    

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
> **SplQueue::dequeue()** - псевдонім [SplDoublyLinkedList::shift()](spldoublylinkedlist.shift.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення видаленого із черги елемента.