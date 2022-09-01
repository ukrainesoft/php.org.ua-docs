---
navigation:
  - arrayiterator.getflags.md: '« ArrayIterator::getFlags'
  - arrayiterator.ksort.md: 'ArrayIterator::ksort »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::key'
---
# ArrayIterator::key

(PHP 5, PHP 7, PHP 8)

ArrayIterator::key — Повертає ключ поточного елемента масиву

### Опис

```methodsynopsis
public ArrayIterator::key(): string|int|null
```

Ця функція повертає ключ поточного елемента масиву

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ поточного елемента у масиві (array).

### Приклади

**Приклад #1 Приклад використання **ArrayIterator::key()****

```php
<?php
$array = array('key' => 'value');

$arrayobject = new ArrayObject($array);
$iterator = $arrayobject->getIterator();

echo $iterator->key(); //key
?>
```
