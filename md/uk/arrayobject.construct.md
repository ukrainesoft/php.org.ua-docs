---
navigation:
  - arrayobject.asort.md: '« ArrayObject::asort'
  - arrayobject.count.md: 'ArrayObject::count »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::\_\_construct

(PHP 5, PHP 7, PHP 8)

ArrayObject::\_\_construct — Створює новий об'єкт масиву

### Опис

public**ArrayObject::\_\_construct**(array|object`$array` \[\], int`$flags`\= 0, string`$iteratorClass`\= ArrayIterator::class)

Створює новий об'єкт масиву.

### Список параметрів

`array`

Параметр`array` приймає значення типу array чи Object.

`flags`

Прапори для керування поведінкою об'єкта [ArrayObject](class.arrayobject.md)Смотрите[ArrayObject::setFlags()](arrayobject.setflags.md)

`iteratorClass`

Вказує клас, який використовуватиметься як ітератор об'єкта [ArrayObject](class.arrayobject.md). Клас має реалізувати інтерфейс [ArrayIterator](class.arrayiterator.md)

### Приклади

**Пример #1 Пример использования**ArrayObject::\_\_construct()\*\*\*\*

```php
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

var_dump($arrayobject);
?>
```

Результат виконання наведеного прикладу:

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

-   [ArrayObject::setflags()](arrayobject.setflags.md) \- Встановлює прапори поведінки
