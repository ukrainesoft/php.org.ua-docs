---
navigation:
  - arrayiterator.offsetunset.md: '« ArrayIterator::offsetUnset'
  - arrayiterator.seek.md: 'ArrayIterator::seek »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::rewind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayIterator::rewind

(PHP 5, PHP 7, PHP 8)

ArrayIterator::rewind — Переміщує покажчик на початок масиву

### Опис

```methodsynopsis
public ArrayIterator::rewind(): void
```

Переміщує покажчик на перший елемент у масиві

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ArrayIterator::rewind()\*\*\*\*

```php
<?php
$arrayobject = new ArrayObject();

$arrayobject[] = 'ноль';
$arrayobject[] = 'один';
$arrayobject[] = 'два';

$iterator = $arrayobject->getIterator();

$iterator->next();
echo $iterator->key(); //1

$iterator->rewind(); // перемещает указатель в начало массива
echo $iterator->key(); //0
?>
```
