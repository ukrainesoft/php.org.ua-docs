---
navigation:
  - appenditerator.getarrayiterator.md: '« AppendIterator::getArrayIterator'
  - appenditerator.getiteratorindex.md: 'AppendIterator::getIteratorIndex »'
  - index.md: PHP Manual
  - class.appenditerator.md: AppendIterator
title: 'AppendIterator::getInnerIterator'
---
# AppendIterator::getInnerIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

AppendIterator::getInnerIterator — Повертає внутрішній ітератор

### Опис

```methodsynopsis
public AppendIterator::getInnerIterator(): Iterator
```

Цей спосіб повертає поточний внутрішній ітератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний внутрішній ітератор або **`null`**, якщо така відсутня.

### Приклади

**Приклад #1 Приклад використання **AppendIterator::getInnerIterator()****

```php
<?php
$array_a = new ArrayIterator(array('a' => 'aardwolf', 'b' => 'bear', 'c' => 'capybara'));
$array_b = new RegexIterator($array_a, '/^[ac]/');

$iterator = new AppendIterator;
$iterator->append($array_a);
$iterator->append($array_b);

foreach ($iterator as $current) {
    $inner = $iterator->getInnerIterator();
    if ($inner instanceOf RegexIterator) {
        echo 'Отфильтрованный: ';
    } else {
        echo 'Оригинальный: ';
    }
    echo $current . PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
Оригинальный: aardwolf
Оригинальный: bear
Оригинальный: capybara
Отфильтрованный: aardwolf
Отфильтрованный: capybara
```

### Дивіться також

-   [AppendIterator::getIteratorIndex()](appenditerator.getiteratorindex.md) - Повертає індекс ітератора
