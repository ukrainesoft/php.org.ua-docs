---
navigation:
  - class.norewinditerator.md: « NoRewindIterator
  - norewinditerator.current.md: 'NoRewindIterator::current »'
  - index.md: PHP Manual
  - class.norewinditerator.md: NoRewindIterator
title: 'NoRewindIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# NoRewindIterator::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

NoRewindIterator::\_\_construct — Створює новий об'єкт NoRewindIterator

### Опис

public **NoRewindIterator::\_\_construct** [Iterator](class.iterator.md) `$iterator`) .

Створює новий об'єкт NoRewindIterator.

### Список параметрів

`iterator`

Ітератор, що використовується.

### Приклади

**Приклад #1 Приклад використання** NoRewindIterator::\_\_construct()\*\*\*\*

Другий цикл нічого не виведе, оскільки ітератор використовується лише один раз і не може бути повернутий на початок.

```php
<?php
$fruit = array('яблоко', 'банан', 'клюква');

$arr = new ArrayObject($fruit);
$it  = new NoRewindIterator($arr->getIterator());

echo "Фрукт А:\n";
foreach( $it as $item ) {
    echo $item . "\n";
}

echo "Фрукт Б:\n";
foreach( $it as $item ) {
    echo $item . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Фрукт А:
яблоко
банан
клюква
Фрукт Б:
```

### Дивіться також

-   [NoRewindIterator::valid()](norewinditerator.valid.md) \- перевіряє ітератор
