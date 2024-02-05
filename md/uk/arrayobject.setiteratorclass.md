---
navigation:
  - arrayobject.setflags.md: '« ArrayObject::setFlags'
  - arrayobject.uasort.md: 'ArrayObject::uasort »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::setIteratorClass'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::setIteratorClass

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

ArrayObject::setIteratorClass — Встановлює ім'я класу ітератора для ArrayObject

### Опис

```methodsynopsis
public ArrayObject::setIteratorClass(string $iteratorClass): void
```

Устанавливает имя класса итератора массива, которое используется[ArrayObject::getIterator()](arrayobject.getiterator.md)

### Список параметрів

`iteratorClass`

Ім'я класу ітератора масиву, який буде використовуватися при ітерації цього об'єкта.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ArrayObject::setIteratorClass()\*\*\*\*

```php
<?php
// Пользовательский ArrayIterator (включает в себя ArrayIterator)
class MyArrayIterator extends ArrayIterator {
    // пользовательская реализация
}

// Массив с количеством фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Устанавливает новое имя класса итератора
$fruitsArrayObject->setIteratorClass('MyArrayIterator');
print_r($fruitsArrayObject->getIterator());

?>
```

Результат виконання наведеного прикладу:

```
MyArrayIterator Object
(
    [lemons] => 1
    [oranges] => 4
    [bananas] => 5
    [apples] => 10
)
```
