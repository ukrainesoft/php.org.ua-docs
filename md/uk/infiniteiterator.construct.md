---
navigation:
  - class.infiniteiterator.md: « InfiniteIterator
  - infiniteiterator.next.md: 'InfiniteIterator::next »'
  - index.md: PHP Manual
  - class.infiniteiterator.md: InfiniteIterator
title: 'InfiniteIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# InfiniteIterator::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

InfiniteIterator::\_\_construct - Конструктор класу InfiniteIterator

### Опис

public **InfiniteIterator::\_\_construct** [Iterator](class.iterator.md) `$iterator`) .

Створює новий об'єкт класу [InfiniteIterator](class.infiniteiterator.md) на основі об'єкта-ітератора [Iterator](class.iterator.md)

### Список параметрів

`iterator`

Нескінченний ітератор.

### Приклади

**Приклад #1 Приклад використання** InfiniteIterator::\_\_construct()\*\*\*\*

```php
<?php
$arrayit  = new ArrayIterator(array('cat','dog'));
$infinite = new InfiniteIterator($arrayit);
$limit    = new LimitIterator($infinite, 0, 7);
foreach($limit as $value)
{
    echo "$value\n";
}
?>
```

Результат виконання наведеного прикладу:

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

-   [InfiniteIterator::next()](infiniteiterator.next.md) \- Переміщує ітератор на одну позицію вперед або на початок
