---
navigation:
  - arrayobject.getiterator.html: '« ArrayObject::getIterator'
  - arrayobject.ksort.html: 'ArrayObject::ksort »'
  - index.html: PHP Manual
  - class.arrayobject.html: ArrayObject
title: 'ArrayObject::getIteratorClass'
---
# ArrayObject::getIteratorClass

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ArrayObject::getIteratorClass — Отримує ім'я класу ітератора для ArrayObject

### Опис

```methodsynopsis
public ArrayObject::getIteratorClass(): string
```

Отримує ім'я класу ітератора масиву, що використовується [ArrayObject::getIterator()](arrayobject.getiterator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я класу ітератора масиву, який використовується для ітерації цього об'єкта.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::getIteratorClass()****

```php
<?php
// Пользовательский ArrayIterator (включает в себя ArrayIterator)
class MyArrayIterator extends ArrayIterator {
    // пользовательская реализация
}

// Масив доступных фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);

// Получить текущее имя класса итератора
$className = $fruitsArrayObject->getIteratorClass();
var_dump($className);

// Установить новое имя класса итератора
$fruitsArrayObject->setIteratorClass('MyArrayIterator');

// Получить новое имя класса итератора
$className = $fruitsArrayObject->getIteratorClass();
var_dump($className);
?>
```

Результат виконання цього прикладу:

```
string(13) "ArrayIterator"
string(15) "MyArrayIterator"
```

### Дивіться також

-   [ArrayObject::setIteratorClass](arrayobject.setiteratorclass.html)
