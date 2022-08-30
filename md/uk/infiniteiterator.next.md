Переміщує ітератор на одну позицію вперед або на початок

-   [« InfiniteIterator::construct](infiniteiterator.construct.html)
    
-   [IteratorIterator »](class.iteratoriterator.html)
    
-   [PHP Manual](index.html)
    
-   [InfiniteIterator](class.infiniteiterator.html)
    
-   Переміщує ітератор на одну позицію вперед або на початок
    

# InfiniteIterator::next

(PHP 5> = 5.1.0, PHP 7, PHP 8)

InfiniteIterator::next — Переміщує ітератор на одну позицію вперед або на початок

### Опис

```methodsynopsis
public InfiniteIterator::next(): void
```

Переміщує внутрішній покажчик об'єкта [Iterator](class.iterator.html) на наступний елемент або перший елемент, якщо поточний елемент був останнім.

> **Зауваження**
> 
> Ітератор [InfiniteIterator](class.infiniteiterator.html) зупиняється, коли об'єкт, що зберігається всередині [Iterator](class.iterator.html) виявляється порожнім.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [InfiniteIterator::construct()](infiniteiterator.construct.html) - Конструктор класу InfiniteIterator