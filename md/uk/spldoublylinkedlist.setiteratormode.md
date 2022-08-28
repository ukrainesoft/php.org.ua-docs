Встановлює режим ітерації

-   [« SplDoublyLinkedList::serialize](spldoublylinkedlist.serialize.html)
    
-   [SplDoublyLinkedList::shift »](spldoublylinkedlist.shift.html)
    
-   [PHP Manual](index.html)
    
-   [SplDoublyLinkedList](class.spldoublylinkedlist.html)
    
-   Встановлює режим ітерації
    

# SplDoublyLinkedList::setIteratorMode

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplDoublyLinkedList::setIteratorMode — Встановлює режим ітерації

### Опис

```methodsynopsis
public SplDoublyLinkedList::setIteratorMode(int $mode): int
```

### Список параметрів

`mode`

Існують два ортогональні набори режимів, які можуть бути встановлені:

-   Напрямок ітерації (одне з двох):
    -   **`SplDoublyLinkedList::IT_MODE_LIFO`** (Стек)
    -   **`SplDoublyLinkedList::IT_MODE_FIFO`** (Черга)
-   Поведінка ітератора (одне із двох):
    -   **`SplDoublyLinkedList::IT_MODE_DELETE`** (Елементи видаляються ітератором)
    -   **`SplDoublyLinkedList::IT_MODE_KEEP`** (Ітератор обходить елементи, не видаляючи їх)

За замовчуванням використовується режим: **`SplDoublyLinkedList::IT_MODE_FIFO`** **`SplDoublyLinkedList::IT_MODE_KEEP`**

### Значення, що повертаються

Повертає різні режими та прапори, що впливають на ітерацію.