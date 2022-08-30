Встановлює режим ітератора

-   [« SplQueue::enqueue](splqueue.enqueue.md)
    
-   [SplHeap »](class.splheap.md)
    
-   [PHP Manual](index.md)
    
-   [SplQueue](class.splqueue.md)
    
-   Встановлює режим ітератора
    

# SplQueue::setIteratorMode

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplQueue::setIteratorMode — Встановлює режим ітератора

### Опис

```methodsynopsis
public SplQueue::setIteratorMode(int $mode): void
```

### Список параметрів

`mode`

Можна змінити лише один параметр ітератора.

-   Поведінка ітератора (чи одне, чи інше):
    -   **`SplDoublyLinkedList::IT_MODE_DELETE`** (Елементи видаляються ітератором)
    -   **`SplDoublyLinkedList::IT_MODE_KEEP`** (Ітератор обходить елементи, не видаляючи їх)

За замовчуванням використовується режим: **`SplDoublyLinkedList::IT_MODE_FIFO`** **`SplDoublyLinkedList::IT_MODE_KEEP`**

**Увага**

Напрямок ітерації не може бути змінено для об'єктів SplQueue, він завжди рівний **`SplDoublyLinkedList::IT_MODE_FIFO`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає [RuntimeException](class.runtimeexception.md) при спробі змінити напрямок ітерації на відмінний від **`SplDoublyLinkedList::IT_MODE_LIFO`**