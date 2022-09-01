---
navigation:
  - arrayobject.asort.md: '« ArrayObject::asort'
  - arrayobject.count.md: 'ArrayObject::count »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::construct'
---
# ArrayObject::construct

(PHP 5, PHP 7, PHP 8)

ArrayObject::construct — Створює новий об'єкт масиву

### Опис

public **ArrayObject::construct**(array | об'єкт `$array` , int `$flags` = 0, string `$iteratorClass` = ArrayIterator::class)

Створює новий об'єкт масиву.

### Список параметрів

`array`

Параметр `array` приймає значення типу array чи Object.

`flags`

Прапори для керування поведінкою об'єкта [ArrayObject](class.arrayobject.md). Дивіться [ArrayObject::setFlags()](arrayobject.setflags.md)

`iteratorClass`

Вказує клас, який використовуватиметься як ітератор об'єкта [ArrayObject](class.arrayobject.md). Клас має реалізувати інтерфейс [ArrayIterator](class.arrayiterator.md)

### Приклади

**Приклад #1 Приклад використання **ArrayObject::construct()****

```php
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

var_dump($arrayobject);
?>
```

Результат виконання цього прикладу:

```
object(ArrayObject)#1 (3) {
  [1]=>
  string(3) "one"
  [2]=>
  string(3) "two"
  [3]=>
  string(5) "three"
}
```

### Дивіться також

-   [ArrayObject::setflags()](arrayobject.setflags.md) - Встановлює прапори поведінки
