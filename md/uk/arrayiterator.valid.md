---
navigation:
  - arrayiterator.unserialize.md: '« ArrayIterator::unserialize'
  - class.cachingiterator.md: CachingIterator »
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::valid'
---
# ArrayIterator::valid

(PHP 5, PHP 7, PHP 8)

ArrayIterator::valid — Перевіряє, чи масив ще запису

### Опис

```methodsynopsis
public ArrayIterator::valid(): bool
```

Перевіряє, чи масив array містить ще записи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо ітератор дійсний і **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ArrayIterator::valid()****

```php
<?php
$array = array('1' => 'one');

$arrayobject = new ArrayObject($array);
$iterator = $arrayobject->getIterator();

var_dump($iterator->valid()); //bool(true)

$iterator->next(); // перемещаем указатель на следующий элемент

//bool(false) потому что в Масиве только один элемент
var_dump($iterator->valid());
?>
```
