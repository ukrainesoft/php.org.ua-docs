---
navigation:
  - class.arrayobject.md: « ArrayObject
  - arrayobject.asort.md: 'ArrayObject::asort »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::append

(PHP 5, PHP 7, PHP 8)

ArrayObject::append — Додає значення до кінця масиву

### Опис

```methodsynopsis
public ArrayObject::append(mixed $value): void
```

Додає нове значення наприкінці масиву.

> **Зауваження** :
> 
> Цей метод не може бути викликаний, якщо [ArrayObject](class.arrayobject.md) був створений із об'єкта. У цьому випадку використовуйте замість нього [ArrayObject::offsetSet()](arrayobject.offsetset.md)

### Список параметрів

`value`

Значення, яке потрібно додати.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ArrayObject::append()\*\*\*\*

```php
<?php
$arrayobj = new ArrayObject(array('first','second','third'));
$arrayobj->append('fourth');
$arrayobj->append(array('five', 'six'));
var_dump($arrayobj);
?>
```

Результат виконання наведеного прикладу:

```
object(ArrayObject)#1 (5) {
  [0]=>
  string(5) "first"
  [1]=>
  string(6) "second"
  [2]=>
  string(5) "third"
  [3]=>
  string(6) "fourth"
  [4]=>
  array(2) {
    [0]=>
    string(4) "five"
    [1]=>
    string(3) "six"
  }
}
```

### Дивіться також

-   [ArrayObject::offsetSet()](arrayobject.offsetset.md) \- Встановлює нове значення за вказаним індексом
