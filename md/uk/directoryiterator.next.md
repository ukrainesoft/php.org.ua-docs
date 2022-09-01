---
navigation:
  - directoryiterator.key.md: '« DirectoryIterator::key'
  - directoryiterator.rewind.md: 'DirectoryIterator::rewind »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::next'
---
# DirectoryIterator::next

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::next — Переміщує курсор на наступний елемент DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::next(): void
```

Переміщує покажчик на наступний елемент [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::next()****

Виведення списку вмісту директорії за допомогою циклу while

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
while($iterator->valid()) {
    echo $iterator->getFilename() . "\n";
    $iterator->next();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
.
..
apple.jpg
banana.jpg
index.php
pear.jpg
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.md) - Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::key()](directoryiterator.key.md) - Повертає ключ поточного елемента DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) - Встановлює покажчик на перший елемент DirectoryIterator
-   [DirectoryIterator::valid()](directoryiterator.valid.md) - Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом
-   [Iterator::next()](iterator.next.md) - Переходить до наступного елементу
