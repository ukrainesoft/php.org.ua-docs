---
navigation:
  - arrayiterator.natsort.md: '« ArrayIterator::natsort'
  - arrayiterator.offsetexists.md: 'ArrayIterator::offsetExists »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayIterator::next

(PHP 5, PHP 7, PHP 8)

ArrayIterator::next — Переміщує покажчик за наступний запис

### Опис

```methodsynopsis
public ArrayIterator::next(): void
```

Переміщує покажчик на наступний запис у масиві.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ArrayIterator::next()\*\*\*\*

```php
<?php
$arrayobject = new ArrayObject();

$arrayobject[] = 'zero';
$arrayobject[] = 'one';

$iterator = $arrayobject->getIterator();

while($iterator->valid()) {
    echo $iterator->key() . ' => ' . $iterator->current() . "\n";

    $iterator->next();
}
?>
```

Результат виконання наведеного прикладу:

```
0 => zero
1 => one
```
