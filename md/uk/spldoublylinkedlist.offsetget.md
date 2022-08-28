Повертає значення за вказаним індексом

-   [« SplDoublyLinkedList::offsetExists](spldoublylinkedlist.offsetexists.html)
    
-   [SplDoublyLinkedList::offsetSet »](spldoublylinkedlist.offsetset.html)
    
-   [PHP Manual](index.html)
    
-   [SplDoublyLinkedList](class.spldoublylinkedlist.html)
    
-   Повертає значення за вказаним індексом
    

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