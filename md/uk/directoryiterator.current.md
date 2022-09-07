---
navigation:
  - directoryiterator.construct.md: '« DirectoryIterator::construct'
  - directoryiterator.getatime.md: 'DirectoryIterator::getATime »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::current'
---
# DirectoryIterator::current

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::current — Повертає поточний елемент DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::current(): mixed
```

Повертає поточний елемент [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний елемент [DirectoryIterator](class.directoryiterator.md)

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::current()****

Приклад виведе список вмісту директорії, що містить скрипт.

```php
<?php
$iterator = new DirectoryIterator(__DIR__);
while($iterator->valid()) {
    $file = $iterator->current();
    echo $iterator->key() . " => " . $file->getFilename() . "\n";
    $iterator->next();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
0 => .
1 => ..
2 => apple.jpg
3 => banana.jpg
4 => index.php
5 => pear.jpg
```

### Дивіться також

-   [DirectoryIterator::key()](directoryiterator.key.md) - Повертає ключ поточного елемента DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.md) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) - Встановлює покажчик на перший елемент DirectoryIterator
-   [DirectoryIterator::valid()](directoryiterator.valid.md) - Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом
-   [Iterator::current()](iterator.current.md) - Повернення поточного елемента
