Отримання внутрішнього об'єкта-ітератора

-   [« LimitIterator::current](limititerator.current.html)
    
-   [LimitIterator::getPosition »](limititerator.getposition.html)
    
-   [PHP Manual](index.html)
    
-   [LimitIterator](class.limititerator.html)
    
-   Отримання внутрішнього об'єкта-ітератора
    

# LimitIterator::getInnerIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

LimitIterator::getInnerIterator — Отримання внутрішнього об'єкта-ітератора

### Опис

```methodsynopsis
public LimitIterator::getInnerIterator(): Iterator
```

Повертає об'єкт-ітератор [Iterator](class.iterator.html) приховані всередині об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Внутрішній об'єкт-ітератор, переданий конструктору [LimitIterator::\_\_construct()](limititerator.construct.html)

### Дивіться також

-   [LimitIterator::\_\_construct()](limititerator.construct.html) - Конструктор класу LimitIterator
-   [IteratorIterator::getInnerIterator()](iteratoriterator.getinneriterator.html) - отримує внутрішній ітератор