- [« ArrayObject::setFlags](arrayobject.setflags.md)
- [ArrayObject::uasort »](arrayobject.uasort.md)

- [PHP Manual](index.md)
- [ArrayObject](class.arrayobject.md)
- Встановлює ім'я класу ітератора ArrayObject

# ArrayObject::setIteratorClass

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

ArrayObject::setIteratorClass — Встановлює ім'я класу ітератора для
ArrayObject

### Опис

public **ArrayObject::setIteratorClass**(string `$iteratorClass`): void

Встановлює ім'я класу ітератора масиву, що використовується
[ArrayObject::getIterator()](arrayobject.getiterator.md).

### Список параметрів

`iteratorClass`
Ім'я класу ітератора масиву, який використовуватиметься під час ітерації
з цього об'єкта.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::setIteratorClass()****

`<?php// Користувальницький ArrayIterator (включає в себе ArrayIterator)class MyArrayIterator extends ArrayIterator {    // користувацька мість|     bananas" => 5, "apples" => 10);$fruitsArrayObject = new ArrayObject($fruits);// Встановлює нове ім'я класу ітератора$fruitsArrayObject->setIteratorClass('$ ));?> `

Результат виконання цього прикладу:

MyArrayIterator Object
(
[lemons] => 1
[oranges] => 4
[bananas] => 5
[apples] => 10
)
