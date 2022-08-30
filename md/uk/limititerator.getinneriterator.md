Отримання внутрішнього об'єкта-ітератора

-   [« LimitIterator::current](limititerator.current.md)
    
-   [LimitIterator::getPosition »](limititerator.getposition.md)
    
-   [PHP Manual](index.md)
    
-   [LimitIterator](class.limititerator.md)
    
-   Отримання внутрішнього об'єкта-ітератора
    

# LimitIterator::getInnerIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

LimitIterator::getInnerIterator — Отримання внутрішнього об'єкта-ітератора

### Опис

```methodsynopsis
public LimitIterator::getInnerIterator(): Iterator
```

Повертає об'єкт-ітератор [Iterator](class.iterator.md) приховані всередині об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Внутрішній об'єкт-ітератор, переданий конструктору [LimitIterator::construct()](limititerator.construct.md)

### Дивіться також

-   [LimitIterator::construct()](limititerator.construct.md) - Конструктор класу LimitIterator
-   [IteratorIterator::getInnerIterator()](iteratoriterator.getinneriterator.md) - отримує внутрішній ітератор