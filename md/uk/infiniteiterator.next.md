Переміщує ітератор на одну позицію вперед або на початок

-   [« InfiniteIterator::construct](infiniteiterator.construct.md)
    
-   [IteratorIterator »](class.iteratoriterator.md)
    
-   [PHP Manual](index.md)
    
-   [InfiniteIterator](class.infiniteiterator.md)
    
-   Переміщує ітератор на одну позицію вперед або на початок
    

# InfiniteIterator::next

(PHP 5> = 5.1.0, PHP 7, PHP 8)

InfiniteIterator::next — Переміщує ітератор на одну позицію вперед або на початок

### Опис

```methodsynopsis
public InfiniteIterator::next(): void
```

Переміщує внутрішній покажчик об'єкта [Iterator](class.iterator.md) на наступний елемент або перший елемент, якщо поточний елемент був останнім.

> **Зауваження**
> 
> Ітератор [InfiniteIterator](class.infiniteiterator.md) зупиняється, коли об'єкт, що зберігається всередині [Iterator](class.iterator.md) виявляється порожнім.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [InfiniteIterator::construct()](infiniteiterator.construct.md) - Конструктор класу InfiniteIterator