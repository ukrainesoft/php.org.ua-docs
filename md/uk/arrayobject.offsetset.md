---
navigation:
  - arrayobject.offsetget.md: '« ArrayObject::offsetGet'
  - arrayobject.offsetunset.md: 'ArrayObject::offsetUnset »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::offsetSet

(PHP 5, PHP 7, PHP 8)

ArrayObject::offsetSet — Встановлює нове значення за вказаним індексом

### Опис

```methodsynopsis
public ArrayObject::offsetSet(mixed $key, mixed $value): void
```

Встановлює нове значення за вказаним індексом.

### Список параметрів

`key`

Індекс для встановлення значення.

`value`

Новое значение для`key`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ArrayObject::offsetSet()\*\*\*\*

```php
<?php
class Example {
    public $property = 'prop:public';
}
$arrayobj = new ArrayObject(new Example());
$arrayobj->offsetSet(4, 'four');
$arrayobj->offsetSet('group', array('g1', 'g2'));
var_dump($arrayobj);

$arrayobj = new ArrayObject(array('zero','one'));
$arrayobj->offsetSet(null, 'last');
var_dump($arrayobj);
?>
```

Результат виконання наведеного прикладу:

```
object(ArrayObject)#1 (3) {
  ["property"]=>
  string(11) "prop:public"
  [4]=>
  string(4) "four"
  ["group"]=>
  array(2) {
    [0]=>
    string(2) "g1"
    [1]=>
    string(2) "g2"
  }
}
object(ArrayObject)#3 (3) {
  [0]=>
  string(4) "zero"
  [1]=>
  string(3) "one"
  [2]=>
  string(4) "last"
}
```

### Дивіться також

-   [ArrayObject::append()](arrayobject.append.md) \- Додає значення в кінець масиву
