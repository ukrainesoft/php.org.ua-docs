---
navigation:
  - arrayobject.count.md: '« ArrayObject::count'
  - arrayobject.getarraycopy.md: 'ArrayObject::getArrayCopy »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::exchangeArray'
---
# ArrayObject::exchangeArray

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ArrayObject::exchangeArray — Замінити масив на інший

### Опис

```methodsynopsis
public ArrayObject::exchangeArray(array|object $array): array
```

Замінює поточний масив (array) іншим масивом (array) чи об'єкт (object).

### Список параметрів

`array`

Новий масив (array) чи об'єкт (object) для заміни поточного масиву.

### Значення, що повертаються

Повертає старий масив (Array).

### Приклади

**Приклад #1 Приклад використання **ArrayObject::exchangeArray()****

```php
<?php
// Масив с количеством фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);
// Масив мест в Европе
$locations = array('Amsterdam', 'Paris', 'London');

$fruitsArrayObject = new ArrayObject($fruits);

// Сейчас заменим фрукты на места
$old = $fruitsArrayObject->exchangeArray($locations);
print_r($old);
print_r($fruitsArrayObject);

?>
```

Результат виконання цього прикладу:

```
Array
(
    [lemons] => 1
    [oranges] => 4
    [bananas] => 5
    [apples] => 10
)
ArrayObject Object
(
    [0] => Amsterdam
    [1] => Paris
    [2] => London
)
```
