Встановлює режим ітератора

-   [« SplStack::\_\_construct](splstack.construct.html)
    
-   [SplQueue »](class.splqueue.html)
    
-   [PHP Manual](index.html)
    
-   [SplStack](class.splstack.html)
    
-   Встановлює режим ітератора
    

# SplStack::setIteratorMode

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplStack::setIteratorMode — Встановлює режим ітератора

### Опис

```methodsynopsis
public SplStack::setIteratorMode(int $mode): void
```

### Список параметрів

`mode`

Можна змінити лише один параметр ітератора.

-   Поведінка ітератора (чи одне, чи інше):
    -   SplDoublyLinkedList::ITMODEDELETE (Елементи видаляються ітератором)
    -   SplDoublyLinkedList::ITMODEKEEP (Ітератор обходить елементи, не видаляючи їх)

За промовчанням використовується режим 0x2 : SplDoublyLinkedList::ITMODELIFO | SplDoublyLinkedList::ITMODEKEEP

**Увага**

Напрямок ітерації не можна змінити для об'єктів SplStack. Спроба зробити це призведе до того, що буде викинуто [RuntimeException](class.runtimeexception.html)

### Значення, що повертаються

Функція не повертає значення після виконання.