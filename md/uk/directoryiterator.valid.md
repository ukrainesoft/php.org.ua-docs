---
navigation:
  - directoryiterator.tostring.md: '« DirectoryIterator::\_\_function toString() { [native code] }'
  - class.emptyiterator.md: EmptyIterator »
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::valid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::valid

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::valid — Перевіряє, чи поточна позиція DirectoryIterator є коректним файлом

### Опис

```methodsynopsis
public DirectoryIterator::valid(): bool
```

Перевіряє, чи є поточна позиція [DirectoryIterator](class.directoryiterator.md) коректним файлом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо позиція коректна, інакше повертає **`false`**

### Приклади

**Пример #1 Пример использования**DirectoryIterator::valid()\*\*\*\*

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));

// Переход к концу итератора
while($iterator->valid()) {
    $iterator->next();
}

$iterator->valid(); // FALSE
$iterator->rewind();
$iterator->valid(); // TRUE

?>
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.md) \- Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::key()](directoryiterator.key.md) \- Повертає ключ для поточного елемента DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) \- Перехід до наступного елементу DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) \- Перемотування ітератора DirectoryIterator назад до початку
-   [Iterator::valid()](iterator.valid.md) \- Перевіряє коректність поточної позиції
