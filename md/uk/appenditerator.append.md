---
navigation:
  - class.appenditerator.md: « AppendIterator
  - appenditerator.construct.md: 'AppendIterator::\_\_construct »'
  - index.md: PHP Manual
  - class.appenditerator.md: AppendIterator
title: 'AppendIterator::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# AppendIterator::append

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

AppendIterator::append — Додає ітератор

### Опис

```methodsynopsis
public AppendIterator::append(Iterator $iterator): void
```

Додає ітератора.

### Список параметрів

`iterator`

Ітератор для додавання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання**AppendIterator::append()\*\*\*\*

```php
<?php
$array_a = new ArrayIterator(array('a', 'b', 'c'));
$array_b = new ArrayIterator(array('d', 'e', 'f'));

$iterator = new AppendIterator;
$iterator->append($array_a);
$iterator->append($array_b);

foreach ($iterator as $current) {
    echo $current;
}
?>
```

Результат виконання наведеного прикладу:

```
abcdef
```

### Дивіться також

-   [AppendIterator::\_\_construct()](appenditerator.construct.md) \- Створює AppendIterator
