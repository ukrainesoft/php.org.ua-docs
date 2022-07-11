- [« ArrayObject::getIterator](arrayobject.getiterator.md)
- [ArrayObject::ksort »](arrayobject.ksort.md)

- [PHP Manual](index.md)
- [ArrayObject](class.arrayobject.md)
- Отримує ім'я класу ітератора для ArrayObject

# ArrayObject::getIteratorClass

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

ArrayObject::getIteratorClass — Отримує ім'я класу ітератора для
ArrayObject

### Опис

public **ArrayObject::getIteratorClass**(): string

Отримує ім'я класу ітератора масиву, який використовується
[ArrayObject::getIterator()](arrayobject.getiterator.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я класу ітератора масиву, який використовується для
ітерації щодо цього об'єкта.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::getIteratorClass()****

`<?php// Користувацький ArrayIterator (включає в себе ArrayIterator)class MyArrayIterator extends ArrayIterator {    // користувацька реалізація}// Массив > " => 5, "apples" => 10);$fruitsArrayObject = new ArrayObject($fruits);// Отримати поточне ім'я класу ітератора$className = $fruitsArrayObject->getIteratorClass нове ім'я класу ітератора$fruitsArrayObject->setIteratorClass('MyArrayIterator');// Отримати нове ім'я класу ітератора$className = $fruitsArrayObject->getIteratorClass();var_dump($className

Результат виконання цього прикладу:

string(13) "ArrayIterator"
string(15) "MyArrayIterator"

### Дивіться також

- [ArrayObject::setIteratorClass](arrayobject.setiteratorclass.md)
