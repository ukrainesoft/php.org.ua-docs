---
navigation:
  - class.filteriterator.md: « FilterIterator
  - filteriterator.construct.md: 'FilterIterator::construct »'
  - index.md: PHP Manual
  - class.filteriterator.md: FilterIterator
title: 'FilterIterator::accept'
---
# FilterIterator::accept

(PHP 5> = 5.1.0, PHP 7, PHP 8)

FilterIterator::accept — Перевіряє, чи поточний елемент ітератора є допустимим.

### Опис

```methodsynopsis
public FilterIterator::accept(): bool
```

Перевіряє, чи поточний елемент ітератора є допустимим для цього фільтра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`** якщо поточний елемент допустимо, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання **FilterIterator::accept()****

```php
<?php
// Этот итератор фильтрует все значения с длиной менее 10 символов
class LengthFilterIterator extends FilterIterator {

    public function accept() {
        // Допускает строки с длиной 10 символов и более
        return strlen(parent::current()) >= 10;
    }

}

$arrayIterator = new ArrayIterator(array('тест1', 'больше 10 символов'));
$lengthFilter = new LengthFilterIterator($arrayIterator);

foreach ($lengthFilter as $value) {
    echo $value . "\n";
}
?>
```

Результат виконання цього прикладу:

```
больше 10 символов
```
