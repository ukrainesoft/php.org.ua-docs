Конструктор класу LimitIterator

-   [« LimitIterator](class.limititerator.md)
    
-   [LimitIterator::current »](limititerator.current.md)
    
-   [PHP Manual](index.md)
    
-   [LimitIterator](class.limititerator.md)
    
-   Конструктор класу LimitIterator
    

# LimitIterator::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

LimitIterator::construct - Конструктор класу LimitIterator

### Опис

public **LimitIterator::construct**[Iterator](class.iterator.md) `$iterator`, int `$offset` = 0, int `$limit`

Створює новий об'єкт класу [LimitIterator](class.limititerator.md) на основі заданого об'єкта `iterator`, початкового зміщення `offset` та максимальної кількості ітерацій `limit`

### Список параметрів

`iterator`

Об'єкт-ітератор [Iterator](class.iterator.md), Число ітерацій якого потрібно обмежити.

`offset`

Необов'язкове початкове усунення.

`limit`

Необов'язкове обмеження кількості ітерацій.

### Помилки

Викидає виняток [ValueError](class.valueerror.md), якщо зміщення `offset` виявиться менше `0`, або якщо `limit` виявиться менше `-1`

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер викидає виняток [ValueError](class.valueerror.md), якщо зміщення `offset` виявиться менше `0`; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |
|  | Тепер викидає виняток [ValueError](class.valueerror.md), якщо зміщення `limit` виявиться менше `-1`; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |

### Приклади

**Приклад #1 Приклад використання **LimitIterator::construct()****

```php
<?php
$ait = new ArrayIterator(array('a', 'b', 'c', 'd', 'e'));
$lit = new LimitIterator($ait, 1, 3);
foreach ($lit as $value) {
    echo $value . "\n";
}
?>
```

Результат виконання цього прикладу:

```
b
c
d
```

### Дивіться також

-   [Приклади використання LimitIterator](class.limititerator.html#limititerator.examples)