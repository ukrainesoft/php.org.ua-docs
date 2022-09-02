---
navigation:
  - arrayiterator.count.md: '« ArrayIterator::count'
  - arrayiterator.getarraycopy.md: 'ArrayIterator::getArrayCopy »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::current'
---
# ArrayIterator::current

(PHP 5, PHP 7, PHP 8)

ArrayIterator::current — Повертає поточний елемент у масиві

### Опис

```methodsynopsis
public ArrayIterator::current(): mixed
```

Повертає поточний елемент у масиві (array).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний елемент у масиві (array).

### Приклади

**Приклад #1 Приклад використання **ArrayIterator::current()****

```php
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

for($iterator = $arrayobject->getIterator();
    $iterator->valid();
    $iterator->next()) {

    echo $iterator->key() . ' => ' . $iterator->current() . "\n";
}
?>
```

Результат виконання цього прикладу:

```
1 => one
2 => two
3 => three
```
