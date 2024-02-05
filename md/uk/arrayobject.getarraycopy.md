---
navigation:
  - arrayobject.exchangearray.md: '« ArrayObject::exchangeArray'
  - arrayobject.getflags.md: 'ArrayObject::getFlags »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::getArrayCopy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::getArrayCopy

(PHP 5, PHP 7, PHP 8)

ArrayObject::getArrayCopy — Створює копію ArrayObject

### Опис

```methodsynopsis
public ArrayObject::getArrayCopy(): array
```

Експортує [ArrayObject](class.arrayobject.md) у масив.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає копію масиву. Якщо [ArrayObject](class.arrayobject.md) посилається на об'єкт, то буде повернено масив властивостей даного об'єкта.

### Приклади

**Пример #1 Пример использования**ArrayObject::getArrayCopy()\*\*\*\*

```php
<?php
// Массив с количеством фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);
$fruitsArrayObject['pears'] = 4;

// Создать копию массива
$copy = $fruitsArrayObject->getArrayCopy();
print_r($copy);

?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [lemons] => 1
    [oranges] => 4
    [bananas] => 5
    [apples] => 10
    [pears] => 4
)
```
