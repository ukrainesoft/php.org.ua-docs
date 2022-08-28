Конструктор класу InfiniteIterator

-   [« InfiniteIterator](class.infiniteiterator.html)
    
-   [InfiniteIterator::next »](infiniteiterator.next.html)
    
-   [PHP Manual](index.html)
    
-   [InfiniteIterator](class.infiniteiterator.html)
    
-   Конструктор класу InfiniteIterator
    

# InfiniteIterator::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

InfiniteIterator::construct - Конструктор класу InfiniteIterator

### Опис

public **InfiniteIterator::construct**[Iterator](class.iterator.html) `$iterator`

Створює новий об'єкт класу [InfiniteIterator](class.infiniteiterator.html) на основі об'єкта-ітератора [Iterator](class.iterator.html)

### Список параметрів

`iterator`

Нескінченний ітератор.

### Приклади

**Приклад #1 Приклад використання **InfiniteIterator::construct()****

```php
<?php
$arrayit  = new ArrayIterator(array('cat','dog'));
$infinite = new InfiniteIterator($arrayit);
$limit    = new LimitIterator($infinite, 0, 7);
foreach($limit as $value)
{
    echo "$value\n";
}
?>
```

Результат виконання цього прикладу:

```
cat
dog
cat
dog
cat
dog
cat
```

### Дивіться також

-   [InfiniteIterator::next()](infiniteiterator.next.html) - Переміщує ітератор на одну позицію вперед або на початок