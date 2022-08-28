Додає/вставляє нове значення за вказаним індексом

-   [« SplDoublyLinkedList](class.spldoublylinkedlist.html)
    
-   [SplDoublyLinkedList::bottom »](spldoublylinkedlist.bottom.html)
    
-   [PHP Manual](index.html)
    
-   [SplDoublyLinkedList](class.spldoublylinkedlist.html)
    
-   Додає/вставляє нове значення за вказаним індексом
    

# SplDoublyLinkedList::add

(PHP 5> = 5.5.0, PHP 7, PHP 8)

SplDoublyLinkedList::add — Додає/вставляє нове значення за вказаним індексом

### Опис

```methodsynopsis
public SplDoublyLinkedList::add(int $index, mixed $value): void
```

Вставляє значення `value` за вказаним індексом `index`. Попереднє значення (і всі наступні) зміщуються вгору за списком.

### Список параметрів

`index`

Індекс, яким треба вставити значення.

`value`

Значення, яке потрібно вставити за індексом `index`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.html), якщо `index` за межами списку, або якщо `index` може бути представлений як цілого числа.