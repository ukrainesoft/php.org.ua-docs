---
navigation:
  - class.limititerator.md: « LimitIterator
  - limititerator.current.md: 'LimitIterator::current »'
  - index.md: PHP Manual
  - class.limititerator.md: LimitIterator
title: 'LimitIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LimitIterator::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

LimitIterator::\_\_construct - Конструктор класу LimitIterator

### Опис

public**LimitIterator::\_\_construct** [Iterator](class.iterator.md) `$iterator`, int`$offset`\= 0, int`$limit`

Створює новий об'єкт класу [LimitIterator](class.limititerator.md) на основі заданого об'єкта `iterator`, начального смещения`offset`и максимального числа итераций`limit`

### Список параметрів

`iterator`

Об'єкт-ітератор [Iterator](class.iterator.md)число ітерацій якого потрібно обмежити.

`offset`

Необов'язкове початкове усунення.

`limit`

Необов'язкове обмеження кількості ітерацій.

### Помилки

Викидає виняток [ValueError](class.valueerror.md), якщо зміщення `offset`окажется меньше , або якщо `limit`окажется меньше`-1`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер викидає виняток [ValueError](class.valueerror.md), якщо зміщення `offset`окажется меньше ; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |
| 8.0.0 | Тепер викидає виняток [ValueError](class.valueerror.md), якщо зміщення `limit`окажется меньше`-1`; раніше викидався виняток [RuntimeException](class.runtimeexception.md) |

### Приклади

**Пример #1 Пример использования**LimitIterator::\_\_construct()\*\*\*\*

```php
<?php
$ait = new ArrayIterator(array('a', 'b', 'c', 'd', 'e'));
$lit = new LimitIterator($ait, 1, 3);
foreach ($lit as $value) {
    echo $value . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
b
c
d
```

### Дивіться також

-   [Приклади використання LimitIterator](class.limititerator.md#limititerator.examples)
